# 📚 Guia Prático de Git, GitHub e Git Flow

## 🔍 Índice
- [Conceitos Básicos](#-conceitos-básicos)
- [Comandos Essenciais](#-comandos-essenciais)
- [Git Flow](#-git-flow)
- [Boa Práticas](#-boas-práticas)

## 🌟 Conceitos Básicos

### Versionamento
- **Master/Main Branch**: Versão estável do projeto
- **Branches**: Ramificações para desenvolvimento paralelo
- **Merge**: Combinação de branches
- **Pull Request**: Solicitação de mesclagem

### Git vs GitHub
| Git | GitHub |
|-----|--------|
| Sistema de controle de versão | Plataforma para hospedar repositórios Git |
| Local | Remoto |
| Linha de comando | Interface web |

## ⌨️ Comandos Essenciais

### Configuração
```bash
git config --global user.name "Seu Nome" # Configura seu NOME
git config --global user.email "seu@email.com" # Configura seu e-mail
```

### Básicos
```bash
  git init                  # Inicia repositório local
  git status                # Verifica estado dos seus arquivos
  git add NOMEARQUIVO       # Adiciona arquivo específico
  git add .                 # Adiciona todos arquivos
  git commit -m "mensagem"  # Cria commit
  git log                   # Mostra histórico dos commits
```
 
### Básicos
```bash
  git branch                  # Lista todas as branches
  git checkout -b nova-branch # Cria nova branch e alterna para a nova branch
  git merge branch            # Combina branches
```
### Remotos
```bash
  git clone URL             # Clona repositório
  git push                  # Envia alterações para a Branch
  git pull                  # Atualiza o repositório local
```

## 🌊 Git Flow

### Inicialização
```bash
  git flow init
```

### Features
```bash
  git flow feature start login
  git flow feature finish login
```

### Release
```bash
  git flow release start 1.0.0
  git flow release finish 1.0.0
```

### Hotfix
```bash
  git flow hotfix start correcao
  git flow hotfix finish correcao
```

## ✅ Boas Práticas

    1. Commits atômicos

        Cada commit deve ter uma única finalidade

        Exemplo: "fix: corrige erro no login"

    2. Nomenclatura

        Branches: feature/nome, fix/nome

        Tags: v1.0.0

## 🔄 Comandos Básicos de Versionamento

| Comando | Explicação | Exemplo Prático |
|---------|------------|-----------------|
| `git init` | Inicia um novo repositório Git no diretório atual | `git init meu-projeto` |
| `git status` | Mostra o estado dos arquivos (rastreados, modificados, etc.) | `git status` |
| `git add` | Adiciona arquivos ao stage (prepara para commit) | `git add .` (todos) ou `git add arquivo.txt` |
| `git rm` | Remove arquivos do tracking do Git | `git rm arquivo.txt` ou `git rm -f arquivo.txt` (forçado) |
| `git commit` | Salva um snapshot das alterações | `git commit -m "Adiciona funcionalidade X"` |

