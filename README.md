[![Run in Insomnia}](https://insomnia.rest/images/run.svg)](https://insomnia.rest/run/?label=fake-api-grupo-4&uri=https%3A%2F%2Ffake-api-grupo-4.onrender.com)

MyRecipes FakeApi - Funcionalidades:

### Register

POST /register

Campos obrigatórios: username, email e password.
Endpoint usado para cadastro de novos usuários

Formato da resposta - STATUS 201 CREATED

(https://drive.google.com/file/d/1DXd4wDXlTV0hkcs5ZX9ngIWG5_dqaljJ/view?usp=sharing)

### Login

POST /login

Campos obrigatórios: email e password.
Endpoint pode ser usado para realizar login com um dos usuários cadastrados na lista de "Users"]

Formato da resposta - STATUS 200 OK

(https://drive.google.com/file/d/1V8aB1Kp-EcfJ_yKMef_eJTR6W4qiCEGD/view?usp=sharing)

### All Users

GET /users

Endpoint usado para fazer autenticação de rotas, necessita autenticação atravéz de um token

Formato da resposta - STATUS 200 OK

(https://drive.google.com/file/d/1y65-783NGnjOvJuqYvwA3H2zhLDU0edj/view?usp=sharing)

### Profile

GET /users/id

Endpoint usado para buscar informações de um usuário especifico e suas receitas, necessita autenticação através de um token

Formato da resposta - STATUS 200 OK

(https://drive.google.com/file/d/1SlMWNeraUniGkjscpIZJR0ox3PKA8VV6/view?usp=sharing)

### Register Recipe

POST /recipes

Endpoint usado para cadastrar uma nova receita de um usuário específico, necessita autenticação através de um token

Formato da resposta - STATUS 201 CREATED

(https://drive.google.com/file/d/1f5WNLvkxyl5Lrlkgkfba8Va3u9Jn3Wf9/view?usp=sharing)

### Edit Recipe

PATCH /recipes/recipeId

Endpoit usado para editar a receita de um usuário específico, necessita autenticação através de um token

Formato da resposta - STATUS 200 OK

(https://drive.google.com/file/d/1ZKw7NHUVuwhVbzrIlVShPo0WuCf137cV/view?usp=sharing)

### All Recipes

GET /recipes

Endpoint usado para buscar todas as receitas sem necessidade de autenticação através de um token

Formato da resposta - STATUS 200 OK

(https://drive.google.com/file/d/1XA3e5lW0kfq4MKd9gbEdXxnrToda2o7h/view?usp=sharing)

### Delete Recipe

DEL /recipes/recipeId

Endpoint usado para excluir uma receita específica, somente quem criou a receita pode excluir, necessita autenticação através de um token

Formato da resposta - STATUS 200 OK

{}
