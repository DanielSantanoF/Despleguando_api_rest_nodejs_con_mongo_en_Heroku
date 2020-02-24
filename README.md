# Despleguando_api_rest_nodejs_con_mongo_en_Heroku


Referencia usada para el repositorio => [Ver](https://elements.heroku.com/buttons/orangemug/heroku-docker-nodejs)

Guia para la asignuatura:
* Sistemas de Gestión Empresarial

Proyecto para despleguar una api rest de nodejs en Heroku

***


## Despleguar nuestra app en Heroku
Deberemos tener Heroku funcional en nuestro ordenador junto a una cuenta y sus credenciales para poder hacer el despliegue [Documentación](https://devcenter.heroku.com/)

El despliegue de esta api rest lo vamos a realizar con docker-compose para ello haremos lo necesario para generar los archivos de Docker como se indica en este otro [Repositorio](https://github.com/DanielSantanoF/Dockerizar_un_api_con_Node.js)

Una vez que tenemos todo lo necesario de docker realizado procederemos a hacer el despliegue en [Heroku](https://devcenter.heroku.com/) ejecutaremos los contenedores de docker con los comandos

```
docker-compose build
docker-compose run --service-ports web bash
```

Tras esto comprobaremos que el api rest funciona y abriremos otro terminal donde haremos el despliegue a Heroku con los comandos
```
heroku create [optional name]
```

Tras crear la aplicación en Heroku en vez de el comando `git push heroku` ejecutaremos el comando
```
heroku container:login
heroku container:push web
heroku container:release
```