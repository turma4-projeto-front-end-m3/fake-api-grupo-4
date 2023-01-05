MyRecipes FakeApi - Funcionalidades:

### Register

POST /register

Campos obrigatórios: username, email e password.
Endpoint usado para cadastro de novos usuários

### Login

POST /login

Campos obrigatórios: email e password.
Endpoint pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"

### Profile

GET /user/id

Endpoint usado para buscar informações de um usuário especifico e suas receitas, necessita autenticação através de um token

### Register Recipe

POST /recipes

Endpoint usado para cadastrar uma nova receita de um usuário específico, necessita autenticação através de um token

### All Recipes

GET /recipes

Endpoint usado para buscar todas as receitas sem necessidade de autenticação através de um token

### Delete Recipe

DEL /recipes/recipeId

Endpoint usado para excluir uma receita específica, somente quem criou a receita pode excluir, necessita autenticação através de um token
