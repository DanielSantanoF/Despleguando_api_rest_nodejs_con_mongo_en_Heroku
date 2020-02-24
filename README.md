# Despleguando_api_rest_nodejs_con_mongo_en_Heroku
Repositorio sobre como desplegar en heroku un api rest de nodejs con express y mongodb

Referencia usada para el repositorio => [Ver](https://elements.heroku.com/buttons/orangemug/heroku-docker-nodejs)

Guia para la asignuatura:
* Sistemas de Gestión Empresarial

Proyecto para despleguar una api rest de nodejs en Heroku

***


## Despleguar nuestra app en Heroku
Deberemos tener Heroku funcional en nuestro ordenador junto a una cuenta y sus credenciales para poder hacer el despliegue [Documentación](https://devcenter.heroku.com/)

El despliegue de esta api rest lo vamos a realizar subiendo nuestra api rest a [Heroku](https://devcenter.heroku.com/) usando un hosting de base de datos de mongodb de [mlab](https://mlab.com/)

Haremos el despliegue a Heroku para ello necesitamos crear una aplicación
```
heroku create [optional name]
```

Tras crear la aplicación en Heroku ejecutaremos los comandos necesarios para subir el repositorio de git a Heroku
```
git init
git add .
git commit -m "<menssage>"
git push heroku master
```

Tras esto en la consola nos saldra un mensaje como este `https://myapp/ deployed to Heroku` la url indicada es la url de tu aplicación despleguada en Heroku

Para acceder a tu aplicación despleguada puedes acceder mediante la url o con el comando de Heroku
```
heroku open
```

Para finalizar tambien podemos ver los logs de la aplicaicón en nuestra consola mediante el comando
```
heroku logs --tail
```