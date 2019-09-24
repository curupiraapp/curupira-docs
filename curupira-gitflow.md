## Curupira - Gitflow

#### Inicializando repositório
- `git init`
- `git add remote origin uri-repositorio`
- verificando origin `git remote -v`
- resetando origin `git rm remote origin`

#### Criar brach de correção
- aba de 'Code' 
- no seletor de branch escreva o nome da nova branch
- clique em create
- no seu repositório local: `git checkout nome-branch`
- caso der erro: `git pull` antes
- `git status` se quiser verificar a branch atual

#### Comitando na branch
- `git add .`
- `git commit -m "msg"`
- `git push`

#### Sincronizando com as alterações na master
- `git pull origin master`
- resolva os conflitos se existirem
- comit as alterações na branch atual

#### Enviando alterações para a master
- solicite pull request
