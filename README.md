# Guia-Git-GitHub-para-Iniciantes
# Git e GitHub para Iniciantes 🚀

Um guia prático para aprender Git e GitHub do zero, com explicações simples, exemplos e comandos para executar no Windows usando o Git Bash.

O objetivo deste projeto é ajudar quem está começando na programação ou na área de tecnologia a entender como criar repositórios, organizar projetos, salvar versões do código e publicar seus arquivos no GitHub.

## 📚 Índice

1. [O que são Git e GitHub?](#1-o-que-são-git-e-github)
2. [Instalando o Git no Windows](#2-instalando-o-git-no-windows)
3. [Configurando o Git](#3-configurando-o-git)
4. [Conhecendo o Git Bash](#4-conhecendo-o-git-bash)
5. [Criando seu primeiro projeto](#5-criando-seu-primeiro-projeto)
6. [Entendendo os principais comandos](#6-entendendo-os-principais-comandos)
7. [Criando um repositório no GitHub](#7-criando-um-repositório-no-github)
8. [Enviando seu projeto para o GitHub](#8-enviando-seu-projeto-para-o-github)
9. [Atualizando um repositório](#9-atualizando-um-repositório)
10. [Clonando um repositório existente](#10-clonando-um-repositório-existente)
11. [Trabalhando com branches](#11-trabalhando-com-branches)
12. [Criando um arquivo .gitignore](#12-criando-um-arquivo-gitignore)
13. [Baixando alterações com git pull](#13-baixando-alterações-com-git-pull)
14. [Erros comuns e soluções](#14-erros-comuns-e-soluções)
15. [Exercícios práticos](#15-exercícios-práticos)
16. [Cola rápida de comandos](#16-cola-rápida-de-comandos)

---

## 1. O que são Git e GitHub?

### Git

Git é um sistema de controle de versão. Ele permite acompanhar as alterações realizadas nos arquivos de um projeto ao longo do tempo.

Com ele, você pode:

- Registrar versões do seu projeto.
- Consultar alterações realizadas.
- Recuperar versões anteriores.
- Trabalhar em diferentes funcionalidades sem alterar diretamente a branch principal.
- Colaborar com outras pessoas.

### GitHub

GitHub é uma plataforma online que hospeda repositórios Git. Com ela, você pode armazenar projetos na nuvem, compartilhar seu código e colaborar com outros desenvolvedores.

**Resumindo:**

- **Git:** controla as versões dos arquivos no seu computador.
- **GitHub:** hospeda seus repositórios online e facilita a colaboração.

## 2. Instalando o Git no Windows

### Passo 1 — Baixar o Git

Acesse o site oficial:

https://git-scm.com/download/win

Baixe e instale o Git for Windows. Para começar, você pode manter as opções padrão do instalador.

### Passo 2 — Abrir o Git Bash

Após a instalação:

1. Abra o menu Iniciar do Windows.
2. Pesquise por `Git Bash`.
3. Abra o terminal.

O Git Bash permite executar comandos do Git e comandos de terminal como `ls`, `cd` e `mkdir`.

### Passo 3 — Verificar a instalação

Execute:

```bash
git --version
```

Se aparecer uma versão do Git, a instalação foi concluída.

## 3. Configurando o Git

Antes de registrar seu primeiro commit, configure seu nome e e-mail.

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
```

Substitua os exemplos pelos seus dados. Prefira um e-mail associado à sua conta do GitHub.

Para conferir as configurações:

```bash
git config --global --list
```

Para utilizar `main` como nome padrão da branch inicial:

```bash
git config --global init.defaultBranch main
```

Essa configuração é realizada uma única vez por usuário do computador, salvo se você precisar alterá-la.

## 4. Conhecendo o Git Bash

Antes de trabalhar com Git, é importante saber navegar pelas pastas.

| Comando | Função |
|---|---|
| `pwd` | Mostra a pasta atual |
| `ls` | Lista arquivos e pastas |
| `ls -la` | Lista também arquivos ocultos |
| `cd nome-da-pasta` | Entra em uma pasta |
| `cd ..` | Volta uma pasta |
| `cd ~` | Vai para a pasta pessoal |
| `mkdir nome` | Cria uma pasta |
| `clear` | Limpa a tela |

### Exemplo

Criando uma pasta para projetos:

```bash
mkdir projetos
cd projetos
pwd
```

O comando `pwd` mostrará o caminho da pasta em que você está.

**Dica:** use a tecla `Tab` para completar nomes de arquivos e pastas automaticamente.

## 5. Criando seu primeiro projeto

Vamos criar um projeto de teste.

### Passo 1 — Criar a pasta

```bash
mkdir meu-primeiro-projeto
cd meu-primeiro-projeto
```

### Passo 2 — Inicializar o Git

```bash
git init -b main
```

Esse comando transforma a pasta atual em um repositório Git, com a branch inicial chamada `main`.

### Passo 3 — Criar um arquivo README

```bash
echo "# Meu primeiro projeto" > README.md
```

O arquivo `README.md` será usado para documentar o projeto.

### Passo 4 — Conferir o estado do repositório

```bash
git status
```

O Git mostrará o arquivo que ainda não está sendo acompanhado pelo histórico.

## 6. Entendendo os principais comandos

O fluxo básico do Git possui três etapas principais.

### 1. Adicionar arquivos à preparação

```bash
git add README.md
```

O `git add` prepara as alterações para o próximo commit.

Para preparar todas as alterações da pasta atual:

```bash
git add .
```

### 2. Registrar uma versão

```bash
git commit -m "Adiciona README inicial"
```

O `git commit` registra no histórico as alterações que foram preparadas.

### 3. Consultar o histórico

```bash
git log --oneline
```

Esse comando mostra os commits em formato resumido.

### Entendendo o fluxo

```text
Editar arquivos
      |
      v
git status
      |
      v
git add .
      |
      v
git commit -m "Mensagem"
      |
      v
Versão registrada localmente
```

**Importante:** o commit salva a versão no repositório local. Para enviá-la ao GitHub, você precisará executar `git push`.

## 7. Criando um repositório no GitHub

### Passo 1 — Acessar o GitHub

Entre em:

https://github.com

Faça login na sua conta.

### Passo 2 — Criar um repositório

1. Clique no botão `+`, no canto superior da página.
2. Selecione `New repository`.
3. Escolha um nome, como `meu-primeiro-projeto`.
4. Adicione uma descrição, se desejar.
5. Escolha entre repositório público ou privado.
6. Clique em `Create repository`.

### Qual opção devo escolher?

- **Public:** qualquer pessoa pode visualizar o repositório.
- **Private:** o acesso fica restrito às pessoas autorizadas.

Para praticar, você pode criar um repositório público sem informações confidenciais.

**Atenção:** se o projeto já existe no seu computador, criar o repositório no GitHub sem adicionar README, licença ou outros arquivos iniciais evita conflitos na primeira publicação.

## 8. Enviando seu projeto para o GitHub

Agora vamos conectar o projeto local ao repositório online.

### Passo 1 — Configurar o endereço remoto

Copie a URL HTTPS do repositório criado no GitHub.

Exemplo:

```bash
git remote add origin https://github.com/SEU-USUARIO/meu-primeiro-projeto.git
```

Substitua `SEU-USUARIO` pelo seu nome de usuário e utilize a URL real do seu repositório.

O nome `origin` é um apelido para o repositório remoto.

### Passo 2 — Conferir o endereço

```bash
git remote -v
```

Esse comando mostra os endereços configurados para buscar e enviar alterações.

### Passo 3 — Preparar e registrar os arquivos

```bash
git add .
git commit -m "Adiciona arquivos iniciais"
```

Se você já fez esse commit anteriormente, não precisa repeti-lo quando não houver novas alterações.

### Passo 4 — Enviar para o GitHub

```bash
git push -u origin main
```

O comando envia os commits locais para a branch `main` no GitHub.

A opção `-u` configura o vínculo entre a branch local e a remota. Nos próximos envios, normalmente basta executar:

```bash
git push
```

### E se aparecer uma tela de login?

Siga as instruções do Git Credential Manager ou do navegador para autenticar sua conta. O GitHub não aceita a senha normal da conta como substituta de autenticação Git via HTTPS.

## 9. Atualizando um repositório

Sempre que você modificar os arquivos, poderá registrar e enviar as alterações.

### Passo 1 — Conferir as alterações

```bash
git status
git diff
```

O `git diff` mostra alterações ainda não preparadas.

### Passo 2 — Preparar os arquivos

```bash
git add .
```

### Passo 3 — Criar um commit

```bash
git commit -m "Atualiza documentação do projeto"
```

### Passo 4 — Enviar para o GitHub

```bash
git push
```

### Fluxo de atualização

```text
Editar → git add . → git commit → git push
```

Repita esse processo sempre que quiser publicar novas versões do seu projeto.

## 10. Clonando um repositório existente

Clonar significa baixar um repositório remoto para o computador, incluindo seu histórico Git.

### Passo 1 — Copiar a URL

No GitHub, abra o repositório e clique em `Code`. Copie a URL HTTPS.

### Passo 2 — Escolher a pasta de destino

No Git Bash, entre na pasta onde deseja armazenar seus projetos.

```bash
cd ~/projetos
```

### Passo 3 — Clonar o repositório

```bash
git clone https://github.com/USUARIO/REPOSITORIO.git
```

Substitua a URL pelo endereço verdadeiro.

### Passo 4 — Entrar na pasta

```bash
cd REPOSITORIO
```

### Passo 5 — Conferir o repositório

```bash
git status
git remote -v
```

O comando `git clone` normalmente já configura o remoto chamado `origin`.

## 11. Trabalhando com branches

Branches permitem desenvolver funcionalidades ou correções separadamente da branch principal.

### Listar as branches

```bash
git branch
```

### Criar uma branch e entrar nela

```bash
git switch -c adiciona-documentacao
```

### Conferir a branch atual

```bash
git branch
```

A branch atual aparece com um asterisco.

### Registrar as alterações

Depois de editar os arquivos:

```bash
git add .
git commit -m "Adiciona nova documentação"
```

### Enviar a branch ao GitHub

```bash
git push -u origin adiciona-documentacao
```

### O que fazer depois?

No GitHub, você pode abrir um Pull Request (PR) para revisar as mudanças e solicitar sua integração à branch principal.

Para voltar à branch principal:

```bash
git switch main
```

**Dica:** para quem está começando, pratique primeiro o fluxo básico antes de estudar merge e resolução de conflitos.

## 12. Criando um arquivo .gitignore

O `.gitignore` informa ao Git quais arquivos e pastas devem ser ignorados quando ainda não estão sendo acompanhados pelo repositório.

Crie um arquivo chamado `.gitignore` na raiz do projeto.

Exemplo:

```gitignore
# Arquivos temporários
*.tmp
*.log

# Configurações locais
.env

# Dependências Python
__pycache__/
venv/

# Dependências Node.js
node_modules/

# Arquivos do Windows
Thumbs.db
Desktop.ini
```

Depois, registre o arquivo:

```bash
git add .gitignore
git commit -m "Adiciona arquivo gitignore"
git push
```

**Atenção:** o `.gitignore` não remove arquivos que já estão sendo acompanhados pelo Git. Ele também não apaga segredos que já foram enviados ao histórico.

Nunca publique senhas, tokens, chaves privadas ou credenciais de serviços.

## 13. Baixando alterações com git pull

O comando `git pull` busca as alterações do repositório remoto e tenta integrá-las à sua branch atual.

```bash
git pull
```

É útil quando você altera arquivos diretamente no GitHub ou trabalha em mais de um computador.

Antes de atualizar, confira:

```bash
git status
```

Se houver alterações locais, verifique se elas estão salvas e commitadas antes de continuar. O Git pode impedir o `pull` quando suas mudanças seriam sobrescritas.

## 14. Erros comuns e soluções

| Erro | Possível solução |
|---|---|
| `fatal: not a git repository` | Entre na pasta correta usando `cd`. |
| `Author identity unknown` | Configure `user.name` e `user.email`. |
| `remote origin already exists` | Confira `git remote -v` e use `git remote set-url origin URL` se precisar corrigir o endereço. |
| `Authentication failed` | Confira o login e a autenticação do GitHub. |
| `Repository not found` | Confira a URL, as permissões e a conta utilizada. |
| `src refspec main does not match any` | Verifique o nome da branch e se já existe um commit. |
| `rejected (fetch first)` | O remoto pode ter commits que ainda não existem localmente. Confira o estado e integre as alterações antes de tentar novamente. |
| `nothing to commit, working tree clean` | Não há alterações detectadas para registrar. |

Se ocorrer um erro, leia a mensagem completa e execute `git status` antes de tentar corrigi-lo.

## 15. Exercícios práticos

### Exercício 1 — Criar um repositório local

- [ ] Criar uma pasta chamada `laboratorio-git`.
- [ ] Executar `git init -b main`.
- [ ] Criar um arquivo `README.md`.
- [ ] Executar `git status`.
- [ ] Adicionar o arquivo com `git add README.md`.
- [ ] Criar um commit.
- [ ] Consultar o histórico com `git log --oneline`.

### Exercício 2 — Publicar no GitHub

- [ ] Criar um repositório vazio no GitHub.
- [ ] Adicionar o remoto com `git remote add origin URL`.
- [ ] Enviar a branch com `git push -u origin main`.
- [ ] Abrir o repositório no navegador.
- [ ] Conferir se o README aparece na página inicial.

### Exercício 3 — Atualizar o projeto

- [ ] Alterar o README.
- [ ] Conferir as mudanças com `git diff`.
- [ ] Executar `git add .`.
- [ ] Criar um novo commit.
- [ ] Executar `git push`.
- [ ] Conferir a atualização no GitHub.

### Exercício 4 — Criar uma branch

- [ ] Executar `git switch -c minha-primeira-branch`.
- [ ] Fazer uma pequena alteração no README.
- [ ] Criar um commit.
- [ ] Enviar a branch ao GitHub.
- [ ] Abrir um Pull Request.

## 16. Cola rápida de comandos

### Configuração

```bash
git --version
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
git config --global --list
```

### Criar e clonar

```bash
git init -b main
git clone URL
```

### Acompanhar alterações

```bash
git status
git diff
git add .
git commit -m "Mensagem do commit"
git log --oneline
```

### GitHub e sincronização

```bash
git remote -v
git remote add origin URL
git push -u origin main
git push
git pull
git fetch
```

### Branches

```bash
git branch
git switch -c nome-da-branch
git switch main
git merge nome-da-branch
```

### Terminal

```bash
pwd
ls -la
cd ..
mkdir nome-da-pasta
clear
```

---

## 🎯 Conclusão

Aprender Git e GitHub é um passo importante para quem deseja entrar na área de tecnologia.

Comece praticando os comandos básicos, crie pequenos projetos e publique suas próprias atividades. Com o tempo, avance para branches, Pull Requests, conflitos e colaboração em equipe.

**O melhor jeito de aprender é praticar, cometer erros em projetos de teste e entender como resolvê-los.**

## 🔗 Links úteis

- [Site oficial do Git](https://git-scm.com/)
- [Download do Git para Windows](https://git-scm.com/download/win)
- [GitHub](https://github.com/)
- [Documentação oficial do Git](https://git-scm.com/doc)
- [GitHub Docs](https://docs.github.com/)
- [GitHub Skills — cursos práticos](https://skills.github.com/)

---

Material criado para fins educacionais e para ajudar iniciantes a aprender Git e GitHub na prática.

Guia Git GitHub para Iniciantes
