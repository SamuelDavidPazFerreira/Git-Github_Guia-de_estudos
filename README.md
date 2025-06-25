# 📚 Guia Prático de Git, GitHub e Git Flow

## 🔍 Índice
- [Conceitos Básicos](#-conceitos-básicos)
- [Comandos Essenciais](#-comandos-essenciais)
- [Git Flow](#-git-flow)
- [Boa Práticas](#-boas-práticas)
- [Recursos Úteis](#-recursos-úteis)

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
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

### Básicos
```bash
  git init                  # Inicia repositório
  git status                # Verifica estado
  git add .                 # Adiciona todos arquivos
  git commit -m "mensagem"  # Cria commit
  git log                   # Mostra histórico
```
 
### Básicos
```bash
  git branch                  # Lista branches
  git checkout -b nova-branch # Cria nova branch
  git merge branch            # Combina branches
```
### Remotos
```bash
  git clone URL             # Clona repositório
  git push origin main      # Envia alterações
  git pull origin main      # Atualiza local
```

## 🌊 Git Flow

### Inicialização
```bash
  git flow init
```
