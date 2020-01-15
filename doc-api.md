## API Curupira

#### URL base: https://api-curupira.firebaseapp.com

#### Obter User ID do app de denúncias:

#### Enviar denúncia:
- request:
  - uri: `/complaints/submit`
  - método: `POST`
  - headers: 
    - **apikey** : string
  - body: `JSON`
    - **type** : string Doméstico/Silvestre
    - **animals** : string com lista de strings sem aspas. ex.: "[Aves, Répteis]"
    - **activities** : string com lista de strings sem aspas. ex.: "[Cativeiro, Maus tratos]"
    - **description** : string
    - **address** : string
    - **cep** : string
    - **date** : long int com timestamp da data selecionada
    - **latitude** : long int
    - **longitude** : long int
    - **userid** : string com id gerado na instalação
    - **debug** : true/false
- response:
  - **status** : 200 OK / 401 Unauthorized / 500 Internal Server Error
  - **dncID** : ID da denúncia
  
#### Obter minhas denúncias:

#### Obter minhas notificações: