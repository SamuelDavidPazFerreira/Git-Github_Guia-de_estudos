# 📚 Guia Prático de Git, GitHub e Git Flow

## 🔍 Índice
- [Conceitos Básicos](#-conceitos-básicos)
- [Comandos Básicos](#-comandos-básicos)
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

## 🔄 Comandos Básicos de Versionamento

| Comando | Explicação | Exemplo Prático |
|---------|------------|-----------------|
| `git init` | Inicia um novo repositório Git no diretório atual | `git init meu-projeto` |
| `git status` | Mostra o estado dos arquivos (rastreados, modificados, etc.) | `git status` |
| `git add` | Adiciona arquivos ao stage (prepara para commit) | `git add .` (todos) ou `git add arquivo.txt` |
| `git rm` | Remove arquivos do tracking do Git | `git rm arquivo.txt` ou `git rm -f arquivo.txt` (forçado) |
| `git commit` | Salva um snapshot das alterações | `git commit -m "Adiciona funcionalidade X"` |

