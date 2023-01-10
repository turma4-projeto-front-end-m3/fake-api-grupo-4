[![Run in Insomnia}](https://insomnia.rest/images/run.svg)](https://insomnia.rest/run/?label=fakeApi-grupo4&uri=https%3A%2F%2Fgithub.com%2Fturma4-projeto-front-end-m3%2Ffake-api-grupo-4%2Fblob%2Fmain%2FfakeApi-grupo4.json)

MyRecipes FakeApi - Funcionalidades:

### Register

POST /register

Campos obrigatórios: username, email e password.
Endpoint usado para cadastro de novos usuários

Formato da resposta - STATUS 201 CREATED

![alt text](./img/respRegUser.jpg)

### Login

POST /login

Campos obrigatórios: email e password.
Endpoint pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"]

Formato da resposta - STATUS 200 OK

![alt text](./img/respLogUser.jpg)

### All Users

GET /users

Endpoint usado para fazer autenticação de rotas, necessita autenticação atravéz de um token

Formato da resposta - STATUS 200 OK

![alt text](./img/respGetAllUsers.jpg)

### Profile

GET /users/id

Endpoint usado para buscar informações de um usuário especifico e suas receitas, necessita autenticação através de um token

Formato da resposta - STATUS 200 OK

![alt text](./img/respGetSpecUser.jpg)

### Register Recipe

POST /recipes

Endpoint usado para cadastrar uma nova receita de um usuário específico, necessita autenticação através de um token

Formato da resposta - STATUS 201 CREATED

![alt text](./img/respRegistRecipe.jpg)

### Edit Recipe

PATCH /recipes/recipeId

Endpoit usado para editar a receita de um usuário específico, necessita autenticação através de um token

Formato da resposta - STATUS 200 OK

![alt text](./img/respEditRecipe.jpg)

### All Recipes

GET /recipes

Endpoint usado para buscar todas as receitas sem necessidade de autenticação através de um token

Formato da resposta - STATUS 200 OK

![alt text](./img/respGARecipes.jpg)

### Delete Recipe

DEL /recipes/recipeId

Endpoint usado para excluir uma receita específica, somente quem criou a receita pode excluir, necessita autenticação através de um token

Formato da resposta - STATUS 200 OK

{}
