## API Curupira

#### URL base: https://api-curupira.firebaseapp.com

#### Enviar denúncia:
- uri: `/complaints/submit`
- método: `POST`
- autenticação: tokenID
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
  - **userID** : string com id gerado na instalação
  - **debug** : true/false
