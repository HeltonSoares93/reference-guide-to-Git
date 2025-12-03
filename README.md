# Tutorial Git: Configuração e Primeiros Passos

Este guia cobre o fluxo essencial para iniciar um projeto, salvar alterações e enviar para o GitHub.

## 1\. Iniciar o Repositório

Abra o terminal na pasta do seu projeto e execute o comando para criar o repositório:

```bash
git init
```

Renomeie a branch principal para o padrão atual (main):

```bash
git branch -M main
```

## 2\. Salvar Alterações (Local)

Adicione todos os arquivos modificados à área de preparação:

```bash
git add .
```

Crie o commit (ponto na história) com uma mensagem descritiva:

```bash
git commit -m "Primeiro commit"
```

## 3\. Conectar ao GitHub (Remoto)

Crie um repositório vazio no GitHub. Copie a URL (HTTPS) e vincule ao seu projeto local:

```bash
git remote add origin <COLE_A_URL_AQUI>
```

Para verificar se a URL ficou correta: (opcional)

```bash
git remote -v
```

## 4\. Enviar Código (Push)

Envie os arquivos e vincule a branch local com a remota:

```bash
git push -u origin main
```

*Nota: Nos próximos envios, basta usar `git push`.*

-----

## Solução de Erros Comuns

### Erro: "Updates were rejected" (Históricos não relacionados)

Se você criou o repositório no GitHub já contendo arquivos (como README ou .gitignore), o comando de push padrão falhará. Escolha uma das soluções abaixo:

**Opção A: Forçar o envio (Substituir)**
Use se quiser apagar o que está no GitHub e manter apenas o que está no seu computador.

```bash
git push -f origin main
```

**Opção B: Mesclar (Unir)**
Use se quiser baixar os arquivos do GitHub e juntar com os seus antes de enviar.

```bash
git pull origin main --allow-unrelated-histories
git push -u origin main
```

-----

Gostaria que eu gerasse um arquivo `.md` com esse conteúdo para você baixar?
