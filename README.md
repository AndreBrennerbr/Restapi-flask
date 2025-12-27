<h1 align="center" style="font-weight: bold;">Flask API 💻</h1>

<p align="center">
 <a href="#tech">Technologies</a> • 
 <a href="#started">Getting Started</a> • 
  <a href="#routes">API Endpoints</a> 
</p>

<p align="center">
    <b>Api para cadastro e busca de usuário com foco em deploy</b>
</p>

<h2 id="technologies">💻 Technologies</h2>

- Python
- Flask
- MongoDB
- Docker
- Docker Compose

<h2 id="started">🚀 Getting started</h2>

<h3>Prerequisites</h3>

- Docker
- Docker Compose


<h3>Cloning</h3>



```bash
git clone https://github.com/AndreBrennerbr/Paas-restapi-flask.git
```

<h3>Config docker-compose variables</h2>

```yaml
SERVICES:
MONGO_INITDB_ROOT_USERNAME={SET_USER_NAME_ON_MONGODB_SERVICES}
MONGO_INITDB_ROOT_PASSWORD={SET_PASSWORD_ON_MONGODB_SERVICES}

API:
MONGODB_USER={USER}
MONGODB_PASSWORD={PASSWORD}
FLASK_ENV={development or prod}
```

<h3>Starting</h3>

```bash
cd Paas-restapi-flask
docker-compose build
docker-compose up
```

<h2 id="routes">📍 API Endpoints</h2>

​
| route               | description                                          
|----------------------|-----------------------------------------------------
| <kbd>GET /users</kbd>     | retrieves users info see [response details](#get-users)
| <kbd>GET /user/:cpf</kbd>     | retrieves user info see [response details](#get-user-cpf)
| <kbd>POST /user</kbd>     | create a new user [request details](#post-user)



<h3 id="get-users">GET /users</h3>

**RESPONSE**
```json
[
 {
   "first_name": "Lucas",
   "last_name": "Silva",
   "cpf": "111.111.111-11",
   "email": "her-email@gmail.com",
   "birth_date": "01/10/2001"
 }
]
```

<h3 id="get-user-cpf">GET /user/:cpf</h3>

**RESPONSE**
```json
{
  "first_name": "Lucas",
  "last_name": "Silva",
  "cpf": "111.111.111-11",
  "email": "her-email@gmail.com",
  "birth_date": "01/10/2001"
}
```

<h3 id="post-user">POST /user</h3>

**REQUEST**
```json
{
  "first_name": "Lucas",
  "last_name": "Silva",
  "cpf": "111.111.111-11",
  "email": "her-email@gmail.com",
  "birth_date": "01/10/2001"
}
```
