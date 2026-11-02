# 📚 Guia de Referência Rápida: Git

Este guia contém os comandos essenciais do Git para o fluxo de trabalho diário de desenvolvimento, desde a configuração inicial até a manipulação de branches e repositórios remotos.

## ⚙️ Configuração Inicial (Setup)

Configure seu usuário e editor padrão ao instalar o Git pela primeira vez.

# Definir nome de usuário global
git config --global user.name "Seu Nome"

# Definir email global
git config --global user.email "seuemail@exemplo.com"

# Verificar as configurações atuais
git config --list
🚀 Iniciando um Projeto
Comandos para começar um novo repositório ou obter um existente.

# Inicializar um repositório Git em uma pasta existente
git init

# Clonar um repositório remoto (baixar para sua máquina)
git clone <url-do-repositorio>
📝 Fluxo de Trabalho Básico (Stage & Commit)
O ciclo de vida básico de alteração de arquivos.


# Verificar o estado dos arquivos (modificados, staged, untracked)
git status

# Adicionar um arquivo específico para a área de preparação (staging)
git add <nome-do-arquivo>

# Adicionar TODOS os arquivos modificados para a área de preparação
git add .

# Gravar as alterações (commit) com uma mensagem descritiva
git commit -m "Mensagem descrevendo o que foi feito"

# Adicionar e commitar em um único passo (apenas para arquivos já rastreados)
git commit -am "Mensagem do commit"
🌿 Trabalhando com Branches
Gerenciamento de ramificações para desenvolvimento paralelo.

# Listar todas as branches locais (a atual estará marcada com *)
git branch

# Criar uma nova branch
git branch <nome-da-branch>

# Mudar para uma branch existente
git checkout <nome-da-branch>
# Ou (versão mais moderna):
git switch <nome-da-branch>

# Criar uma branch e mudar para ela imediatamente
git checkout -b <nome-da-nova-branch>

# Mesclar uma branch na branch atual
git merge <nome-da-branch>
☁️ Sincronizando com Remoto (Sync)
Interação com repositórios hospedados (GitHub, GitLab, Azure DevOps, etc).

# Baixar alterações do remoto sem aplicar (apenas atualiza referências)
git fetch

# Baixar alterações e mesclar automaticamente na branch atual
git pull origin <nome-da-branch>

# Enviar seus commits locais para o repositório remoto
git push origin <nome-da-branch>

# Enviar uma branch nova pela primeira vez (definindo upstream)
git push -u origin <nome-da-branch>
🔍 Inspeção e Histórico
Comandos para visualizar o que aconteceu no projeto.

# Visualizar o histórico de commits
git log

# Visualizar o histórico de forma resumida (uma linha por commit)
git log --oneline

# Ver diferenças entre o diretório de trabalho e o último commit
git diff
↩️ Desfazendo Alterações (Use com Cuidado)

# Desfazer alterações em um arquivo (restaurar para o último commit)
git checkout -- <arquivo>
# Ou:
git restore <arquivo>

# Remover arquivos da área de staging (desfazer o 'git add')
git reset HEAD <arquivo>
# Ou:
git restore --staged <arquivo>

# Reverter um commit específico criando um novo commit inverso
git revert <hash-do-commit>

<!-- sync: repository update -->
