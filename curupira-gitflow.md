## Curupira - Gitflow

### Fluxo básico

1. Criar branch
2. Aplicar correções
3. Verificar alterações com a master
4. Testar
5. Alterar código de versão e nome
6. Enviar alterações para a master
7. Gerar APKs
8. Atualizar Release Notes
9. Enviar para produção

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

#### Sincronizando com as alterações da master (Outra branch foi merged)
- `git pull origin master`
- resolva os conflitos se existirem
- comit as alterações na branch atual

#### Realização de testes
- Testar todos os casos de uso possíveis e em diferentes dipositivos

#### Enviando alterações para a master
- verifique se todas as alterações locais estão sincronizadas com sua branch no GitHub
- sincronize sua branch com as alterações da master se existir
- altere o 'versionCode' e 'versionName' em app -> build.gradle
- na aba 'Pull requests'
- em 'New pull requests'
- selecione a branch base como master e a branch compare como sua-branch
- Aguarde verficação do merge
- Se der conflito: sincronize seu repositório com a master manualmente, commit e tente novamente
- Caso não haja conflitos: revise as alterações apresentadas e clique em 'Create pull request'
- Escreva um breve resumo da alteração e 'Create pull request'
- Em seguida faça o merge das branchs em 'Merge pull request'
- Caso tenha dado tudo certo, você tem a opção de deletar a branch de correção

#### Gerar APKs
- verifique se alterou o 'versionCode' e 'versionName' em app -> build.gradle
- no Android Studio
- build -> Create Signed APKs -> APKs
- Selecione o arquivo curupira.jks e preencha os dados
- Selecione 'release'

#### Atualizar Release notes
- No repositório https://github.com/curupiraapp/curupira-docs
- Atualize o arquivo correspondente ao App alterado

#### Enviar pra Google Play
- Em https://play.google.com/apps/publish
- Selecione o App alterado
- Na aba 'Gerenciamento de versão' -> 'Versões de apps'
- 'Gerenciar' na faixa de produção
- 'Criar uma versão'
- Selecione o APK
- Insira o nome da versão (mesmo do gradle)
- Insira a nota de versão que irá aparecer na página do App Google Play
- 'Salvo' e em seguida 'Revisar'
- Verique se gerou algum erro ou aviso na revisão no topo da página
- Caso contrário: 'Iniciar publicação'
- Verifique o final do processamento na aba 'Painel'





