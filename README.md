# Meu Guia Completo de Git, GitHub e Git Flow

## Aqui estão minhas anotações detalhadas sobre versionamento de código, Git, GitHub e Git Flow, com exemplos práticos para cada comando!
### 🔄 O que é Versionamento?

    Motivação:

    Trabalhar em equipe sem controle de versão = caos garantido!

    Versionamento te dá visibilidade total das mudanças no projeto

    Histórico organizado de todas as alterações

### Conceito-chave: Master Branch
É a branch principal, a versão estável do projeto. Nunca codificamos diretamente nela! O fluxo ideal:

    Criamos uma nova branch a partir da master

    Desenvolvemos nosso código nessa nova branch

    Fazemos um merge (combinação de branches) via pull request (solicitação de mesclagem)

###🐙 O que é o Git?

Ferramenta de controle de versão criada por Linus Torvalds (o mesmo criador do Linux). Permite:

    Rastrear mudanças no código

    Trabalhar em equipe de forma organizada

    Voltar no tempo se algo der errado

### 🌎 O que é GitHub?

Plataforma online que hospeda repositórios Git. Funciona como um "Facebook para códigos" onde você pode:

    Visualizar histórico de commits

    Gerenciar branches

    Controlar releases (versões estáveis marcadas por tags)

    Ver contribuidores do projeto

### 🌊 O que é Git Flow?

    Conjunto de comandos que automatizam fluxos comuns no Git. É como um "atalho inteligente" para não precisar decorar sequências longas de comandos.
    
### 🌿 Como funcionam branches?

Estrutura ideal:
text

master (produção)
  ↑
release (versões)
  ↑
develop (desenvolvimento)
  ↑
feature/* (novas funcionalidades)

Tipos de branches:

    Feature: Para desenvolver novas funcionalidades

    Release: Preparação para versão nova

    Hotfix: Correções emergenciais em produção

🔄 Rebase vs Merge
	Merge	Rebase
O que faz	Cria commit de junção	Reescreve histórico
Quando usar	Quando histórico precisa ser preservado	Para limpar histórico antes do merge
Exemplo	git merge feature	git rebase main

Merge: Mantém o histórico exato, mas pode ficar poluído
Rebase: Cria histórico linear, mas "reescreve" commits
📝 Comandos Básicos do Git
Configuração Inicial
bash

git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"

Iniciando um Repositório
bash

# Cria um novo repositório
git init
# Exemplo: git init meu-projeto

# Verifica status dos arquivos
git status

Trabalhando com Arquivos
bash

# Adiciona arquivos para commit
git add arquivo.txt
git add .  # Adiciona todos os arquivos

# Remove arquivos do tracking
git rm arquivo.txt
git rm -f arquivo.txt  # Força remoção

# Desfaz alterações antes do add
git checkout -- arquivo.txt

Commits
bash

# Cria um commit
git commit -m "mensagem descritiva"
# Exemplo: git commit -m "Adiciona funcionalidade de login"

# Ver histórico de commits
git log
git log --oneline  # Versão resumida

Branches
bash

# Cria e muda para nova branch
git checkout -b nova-feature
# Ou com o novo comando:
git switch -c nova-feature

# Lista branches
git branch
git branch -a  # Mostra remotas também

# Alterna entre branches
git checkout main
git switch main  # Forma mais nova

Trabalhando com Remotos
bash

# Clona um repositório
git clone https://github.com/usuario/repositorio.git

# Envia alterações para o remoto
git push origin main

# Atualiza repositório local
git pull origin main
# Ou separadamente:
git fetch  # Baixa alterações
git merge  # Combina com local

Merge e Conflitos
bash

# Faz merge de uma branch
git merge feature/login

# Se houver conflitos:
# 1. Edite os arquivos marcados
# 2. git add arquivo-conflitado
# 3. git commit

Tags e Versões
bash

# Cria uma tag
git tag v1.0.0
git tag -a v1.0.0 -m "Versão 1.0.0"

# Envia tags para remoto
git push origin --tags

Desfazendo Coisas
bash

# Desfaz alterações não commitadas
git restore arquivo.txt

# Remove arquivos não rastreados
git clean -fd

# Altera último commit
git commit --amend

# Volta para commit específico
git reset --hard HASH_DO_COMMIT

🚀 Comandos Git Flow
Inicialização
bash

git flow init
# Responde as perguntas sobre nomes de branches

Feature Branches
bash

# Inicia nova feature
git flow feature start login

# Publica feature
git flow feature publish login

# Finaliza feature (merge em develop)
git flow feature finish login

Release Branches
bash

# Inicia nova release
git flow release start 1.2.0

# Publica release
git flow release publish 1.2.0

# Finaliza release (merge em main e develop)
git flow release finish 1.2.0

Hotfix Branches
bash

# Inicia hotfix
git flow hotfix start correcao-login

# Finaliza hotfix (merge em main e develop)
git flow hotfix finish correcao-login

📌 Git Ignore

Arquivo .gitignore especifica quais arquivos/diretórios o Git deve ignorar. Exemplo:
text

# Ignora arquivos de log
*.log

# Ignora pasta de dependências
node_modules/

# Ignora arquivos de ambiente
.env

💡 Dicas Pró

    Commits atômicos: Cada commit deve representar uma única mudança lógica

    Mensagens claras: Use o padrão: "Tipo: Descrição" (ex: "feat: Adiciona login com Google")

    Pull Requests: Sempre revise código antes de merge

    Rebase local: Use antes de push para manter histórico limpo

    .gitignore: Configure desde o início para não commitar arquivos desnecessários

🔄 Fluxo de Trabalho Típico

    git pull origin main - Atualiza seu local

    git checkout -b feature/nova - Cria branch para feature

    Desenvolve e testa

    git add . e git commit -m "mensagem"

    git push origin feature/nova

    Abre Pull Request no GitHub

    Após aprovação, faz merge

    git checkout main e git pull para atualizar

Espero que este guia ajude em sua jornada com Git! Lembre-se: a prática leva à perfeição. 🚀
