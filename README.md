# 📚 Guia Prático de Git, GitHub e Git Flow

## 🔍 Índice
- [Conceitos Básicos](#-conceitos-básicos)
- [Comandos Básicos de Versionamento](#-comandos-básicos-de-versionamento)
- [Git Flow](#-git-flow)

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

## 🌿 Gerenciamento de Branches

| Comando | Explicação | Exemplo Prático |
|---------|------------|-----------------|
| `git checkout` | Alterna entre branches ou desfaz alterações | `git checkout main` ou `git checkout -- arquivo.txt` |
| `git checkout -b` | Cria e muda para nova branch | `git checkout -b feature/login` |
| `git switch` | Alterna entre branches (versão mais nova) | `git switch main` |
| `git switch -c` | Cria e muda para nova branch | `git switch -c hotfix/pagamento` |

## ☁️ Trabalhando com Repositórios Remotos

| Comando | Explicação | Exemplo Prático |
|---------|------------|-----------------|
| `git clone` | Copia um repositório remoto para local | `git clone https://github.com/user/repo.git` |
| `git push` | Envia commits para o repositório remoto | `git push origin main` |
| `git pull` | Atualiza o repositório local com alterações remotas | `git pull origin develop` |
| `git fetch` | Busca alterações remotas sem mesclar | `git fetch --all` |

## 🔀 Integração de Código

| Comando | Explicação | Exemplo Prático |
|---------|------------|-----------------|
| `git merge` | Combina branches | `git merge feature/login` (estando na branch de destino) |
| `git cherry-pick` | Copia um commit específico para a branch atual | `git cherry-pick abc1234` |
| `git rebase` | Reaplica commits em outra base | `git rebase main` (estando na feature branch) |

## ⏪ Desfazendo Alterações

| Comando | Explicação | Exemplo Prático |
|---------|------------|-----------------|
| `git reset` | Volta para um commit específico | `git reset --hard HEAD~1` (volta 1 commit) |
| `git restore` | Desfaz alterações em arquivos | `git restore arquivo.txt` |
| `git clean` | Remove arquivos não rastreados | `git clean -fd` (remove diretórios e arquivos) |
| `git stash` | Guarda alterações temporariamente | `git stash` e `git stash pop` |

## 🏷️ Versionamento com Tags

| Comando | Explicação | Exemplo Prático |
|---------|------------|-----------------|
| `git tag` | Cria/mostra tags para marcar versões | `git tag v1.0.0` |
| `git push --tags` | Envia tags para o repositório remoto | `git push origin --tags` |

## 🔍 Inspeção do Histórico

| Comando | Explicação | Exemplo Prático |
|---------|------------|-----------------|
| `git log` | Mostra histórico de commits | `git log --oneline --graph` (visual compacto) |
| `git diff` | Mostra diferenças entre versões | `git diff HEAD~1 HEAD` (últimas alterações) |

## 💡 Dicas de Uso

1. **Commits Atômicos**: Cada commit deve representar uma única alteração lógica
   ```bash
   git add arquivo1.txt
   git commit -m "Corrige bug no cálculo de impostos"

## 🌊 Git Flow

| Comando | Explicação | Exemplo Prático | Equivalente Git |
|---------|------------|-----------------|-----------------|
| `git flow init` | Inicializa um novo repositório com estrutura Git Flow | `git flow init` (usa padrões) | Configura branches main/develop |
| `git flow feature start [nome]` | Cria nova branch de feature a partir de develop | `git flow feature start login` | `git checkout -b feature/login develop` |
| `git flow feature finish [nome]` | Faz merge da feature em develop e remove a branch | `git flow feature finish login` | `git checkout develop && git merge feature/login && git branch -d feature/login` |
| `git flow feature publish [nome]` | Publica a branch de feature no repositório remoto | `git flow feature publish login` | `git push -u origin feature/login` |
| `git flow release start [versão]` | Cria branch de release a partir de develop | `git flow release start 1.0.0` | `git checkout -b release/1.0.0 develop` |
| `git flow release finish [versão]` | Finaliza release com merge em main e develop + tag | `git flow release finish 1.0.0` | `git checkout main && git merge release/1.0.0 && git tag -a 1.0.0` |
| `git flow hotfix start [nome]` | Cria branch de hotfix a partir de main | `git flow hotfix start correcao` | `git checkout -b hotfix/correcao main` |
| `git flow hotfix finish [nome]` | Finaliza hotfix com merge em main e develop + tag | `git flow hotfix finish correcao` | `git checkout main && git merge hotfix/correcao && git tag -a hotfix-correcao` |

## Dicas de Uso Prático

Padrão de Nomenclatura:
```bash

# Features
git flow feature start user-authentication

# Releases
git flow release start 2.1.3

# Hotfixes
git flow hotfix start security-patch
