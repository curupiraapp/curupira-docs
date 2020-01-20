# API Curupira

#### URL base: https://api-curupira.firebaseapp.com

- [Usuários](#usuarios)
  - [Obter User ID anônimo](#obter-user-id-anônimo)
- [Denúncias](#denúncias)
  - [Enviar denúncia](#enviar-denúncia)
  - [Obter denúncia pelo ID](#obter-denúncia-pelo-id)
  - [Obter denúncias por usuário](#obter-denúncias-por-usuário)

## Usuários

#### Obter User ID anônimo:
- request:
  - uri: `/users/anonymous/create`
  - método: `GET`
  - headers: 
    - **apikey** : string
  - body: No body
- response: `JSON`
  - **status** : 200 OK / 401 Unauthorized / 500 Internal Server Error
  - **user_id** : ID da usuário para ser enviado juntamente com as denúncias

## Denúncias

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
- response: `JSON`
  - **status** : 200 OK / 401 Unauthorized / 500 Internal Server Error
  - **complaint_id** : ID da denúncia
  
#### Obter denúncia pelo ID:
- request:
  - uri: `/complaints/{id}`
  - método: `GET`
  - headers: 
    - **apikey** : string
  - body: No body
- response: `JSON`
  - **type** : string Doméstico/Silvestre
  - **animals** : string com lista de strings sem aspas. ex.: "[Aves, Répteis]"
  - **activities** : string com lista de strings sem aspas. ex.: "[Cativeiro, Maus tratos]"
  - **description** : string
  - **address** : string
  - **cep** : string
  - **date** : long int com timestamp da data selecionada
  - **latitude** : long int
  - **longitude** : long int
  - **count_audios** : int
  - **count_imgs** : int
  - **state** : string Em espera/Encaminhada/Averiguada
  - **protocol** : string com protocolo do associado pelo Ibama
  - **userid** : string com ID do user remetente
  - **created_at** : long int com timestamp da data de envio

#### Obter denúncias por usuário:
- request:
  - uri: `/complaints/user/{userid}`
  - método: `GET`
  - headers: 
    - **apikey** : string
  - body: No body
- response: `JSON`
  - lista de objetos com a mesma estrutura da pesquisa por ID.
