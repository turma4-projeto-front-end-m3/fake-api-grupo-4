[![Run in Insomnia}](https://insomnia.rest/images/run.svg)](https://insomnia.rest/run/?label=fake-api-grupo-4&uri=https%3A%2F%2Ffake-api-grupo-4.onrender.com)

MyRecipes FakeApi - Funcionalidades:

### Register

POST /register

Campos obrigatórios: username, email e password.
Endpoint usado para cadastro de novos usuários

Formato da resposta - STATUS 201 CREATED

{
"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImpvYW9AbWFpbC5jb20iLCJpYXQiOjE2NzI4NDIxNjQsImV4cCI6MTY3Mjg0NTc2NCwic3ViIjoiMiJ9.Paz2qeBwuuDMvhuNU1DeutwVcU_4z68Yw9Q-wiVLQ4c",
"user": {
"email": "joao@mail.com",
"username": "joao",
"imgUrl": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fbr.depositphotos.com%2Fstock-photos%2Falgu%25C3%25A9m.html&psig=AOvVaw2EYPW7T2rhBREON5pPYdZq&ust=1672928244358000&source=images&cd=vfe&ved=0CA8QjRxqFwoTCMjk372NrvwCFQAAAAAdAAAAABAI",
"id": 2
}
}

### Login

POST /login

Campos obrigatórios: email e password.
Endpoint pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"]

Formato da resposta - STATUS 200 OK

{
"accessToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJlbWFpbCI6ImpvYW9AbWFpbC5jb20iLCJpYXQiOjE2NzMxMDY5OTksImV4cCI6MTY3MzExMDU5OSwic3ViIjoiMiJ9.DCge0tXAdmD1MmQlco-TkdTYixcZLdJzrfHDiDzcFu0",
"user": {
"email": "joao@mail.com",
"username": "joao",
"imgUrl": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fbr.depositphotos.com%2Fstock-photos%2Falgu%25C3%25A9m.html&psig=AOvVaw2EYPW7T2rhBREON5pPYdZq&ust=1672928244358000&source=images&cd=vfe&ved=0CA8QjRxqFwoTCMjk372NrvwCFQAAAAAdAAAAABAI",
"id": 2
}
}

### All Users

GET /users

Endpoint usado para fazer autenticação de rotas, necessita autenticação atravéz de um token

Formato da resposta - STATUS 200 OK

[
{
"email": "jose@mail.com",
"password": "$2a$10$MiKYG/1erYBpuOzyYRrKSeD08T2OGXC7cYi1eX4MTW5wj9Etcd8M6",
"username": "jose",
"imgUrl": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.pexels.com%2Fpt-br%2Fprocurar%2Fpessoa%2F&psig=AOvVaw2EYPW7T2rhBREON5pPYdZq&ust=1672928244358000&source=images&cd=vfe&ved=0CA8QjRxqFwoTCMjk372NrvwCFQAAAAAdAAAAABAE",
"id": 1
},
{
"email": "joao@mail.com",
"password": "$2a$10$kQ6UEM4hXBmwv5Liu8.ZEuH8ipWnPqKJerW4RT9jUtbJpUuKUTKHm",
"username": "joao",
"imgUrl": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fbr.depositphotos.com%2Fstock-photos%2Falgu%25C3%25A9m.html&psig=AOvVaw2EYPW7T2rhBREON5pPYdZq&ust=1672928244358000&source=images&cd=vfe&ved=0CA8QjRxqFwoTCMjk372NrvwCFQAAAAAdAAAAABAI",
"id": 2
}
]

### Profile

GET /users/id

Endpoint usado para buscar informações de um usuário especifico e suas receitas, necessita autenticação através de um token

Formato da resposta - STATUS 200 OK

{
"email": "joao@mail.com",
"password": "$2a$10$kQ6UEM4hXBmwv5Liu8.ZEuH8ipWnPqKJerW4RT9jUtbJpUuKUTKHm",
"username": "joao",
"imgUrl": "https://www.google.com/url?sa=i&url=https%3A%2F%2Fbr.depositphotos.com%2Fstock-photos%2Falgu%25C3%25A9m.html&psig=AOvVaw2EYPW7T2rhBREON5pPYdZq&ust=1672928244358000&source=images&cd=vfe&ved=0CA8QjRxqFwoTCMjk372NrvwCFQAAAAAdAAAAABAI",
"id": 2,
"recipes": []
}

### Register Recipe

POST /recipes

Endpoint usado para cadastrar uma nova receita de um usuário específico, necessita autenticação através de um token

Formato da resposta - STATUS 201 CREATED

{
"recipeName": "Lasanha",
"category": "Massas",
"ingredients": [
{
"ingredientName": "tomate",
"qty": "300g",
"unity": "2"
}
],
"prepTime": "1 hora e 20 minutos",
"portions": 2,
"description": "adicione farinha...",
"userId": 1,
"id": 1
}

### All Recipes

GET /recipes

Endpoint usado para buscar todas as receitas sem necessidade de autenticação através de um token

Formato da resposta - STATUS 200 OK

[
{
"recipeName": "Lasanha",
"category": "Massas",
"ingredients": [
{
"ingredientName": "batata",
"qty": "200g",
"unity": "2"
}
],
"prepTime": "1 hora e 25 minutos",
"portions": 2,
"description": "Blablo blablo",
"userId": 1,
"id": 1
}
]

### Delete Recipe

DEL /recipes/recipeId

Endpoint usado para excluir uma receita específica, somente quem criou a receita pode excluir, necessita autenticação através de um token

Formato da resposta - STATUS 200 OK

{}
