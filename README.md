# Versionamento e Git/GitHub - Guia de Estudo
## O que é Versionamento?

Versionamento (ou controle de versão) é um sistema que registra mudanças em arquivos ao longo do tempo, permitindo que você recupere versões específicas mais tarde.
Motivação para usar versionamento:

    Colaboração: Projetos com muitas pessoas ficam organizados com versionamento

    Visão global: Você tem controle sobre o que entra e sai no seu projeto

    Histórico: Acompanhamento fácil de todas as mudanças no projeto

    Segurança: Possibilidade de reverter para versões anteriores se necessário

Conceitos fundamentais:

    Master/Main Branch: É o branch principal que contém a versão estável do projeto

    Branch: Uma linha de desenvolvimento separada da principal (cópia da Master)

    Merge: Processo de combinar o histórico de duas ou mais branches em uma única

    Pull Request: Solicitação para mesclar um branch com o branch principal (Master)

Fluxo básico de trabalho:

    Cria-se um novo branch a partir da Master

    Desenvolve-se as alterações nesse branch

    Faz-se um pull request para propor a integração com a Master

    Após revisão, o merge é realizado

## O que é o Git?

Git é um sistema de controle de versão distribuído criado por Linus Torvalds em 2005 para o desenvolvimento do kernel Linux.

Principais características:

    Distribuído: Cada desenvolvedor tem uma cópia completa do repositório

    Rápido: Projetado para eficiência com grandes projetos

    Seguro: Usa SHA-1 para garantir integridade dos dados

    Flexível: Suporta diversos fluxos de trabalho

## O que é GitHub?

GitHub é uma plataforma de hospedagem de código baseada em Git com recursos adicionais:

    Repositórios: Espaços para cada projeto (públicos ou privados)

    Visualização: Interface para acompanhar o histórico do projeto

    Colaboração: Ferramentas para trabalho em equipe

    Recursos adicionais:

        Issues (gerenciamento de tarefas)

        Pull requests (revisão de código)

        Actions (automação CI/CD)

        Wiki (documentação)

        Pages (hospedagem de sites)

No GitHub você pode visualizar:

    Histórico de commits

    Branches existentes

    Releases (versões estáveis marcadas com tags)

    Contribuidores do projeto

## O que é Git Flow?

Git Flow é uma metodologia (conjunto de convenções) para organização de branches que define:

    Branches principais:

        main/master (produção)

        develop (próxima versão)

    Branches de apoio:

        feature/* (novas funcionalidades)

        release/* (preparação para lançamento)

        hotfix/* (correções urgentes)

Embora não seja obrigatório, o Git Flow ajuda a manter um fluxo organizado, especialmente em projetos maiores.

## Comandos Git essenciais

Configuração inicial
bash

git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"

## Comandos básicos
bash

### Inicia um novo repositório Git
git init

### Verifica o status dos arquivos
git status

### Adiciona arquivos para o próximo commit
git add nome_do_arquivo      # Arquivo específico
git add .                    # Todos os arquivos modificados

### Remove arquivos do tracking do Git
git rm nome_do_arquivo       # Remove e para de trackear
git rm --cached nome_do_arquivo # Para de trackear mas mantém o arquivo
git rm -f nome_do_arquivo    # Força remoção de arquivo não enviado ao servidor

### Cria um commit com as alterações
git commit -m "Mensagem descritiva"

### Desfaz alterações locais antes do add
git checkout -- nome_do_arquivo

### Visualiza o histórico de commits
git log

Trabalhando com branches
bash

### Lista todos os branches
git branch

### Cria um novo branch
git branch nome_do_branch

### Muda para um branch existente
git checkout nome_do_branch

### Cria e muda para um novo branch
git checkout -b nome_do_branch

### Mescla um branch com o atual
git merge nome_do_branch

### Deleta um branch
git branch -d nome_do_branch

Trabalhando com repositórios remotos
bash

### Adiciona um repositório remoto
git remote add origin URL_DO_REPOSITORIO

### Envia commits para o repositório remoto
git push -u origin nome_do_branch

### Atualiza o repositório local com alterações remotas
git pull origin nome_do_branch

### Clona um repositório existente
git clone URL_DO_REPOSITORIO
