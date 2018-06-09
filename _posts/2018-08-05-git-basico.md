---
layout: post
title: Aprende lo básico en Git y Github
tags: [HTML, CSS, Github]
excerpt_separator: <!--more-->
---

En este artículo veremos como se realiza el proceso para llevar nuestro proyecto a Github, el cual aprenderemos a usar los comandos básicos para crear y subir nuestro primer repositorio.

Para tal uso primero debemos de crear un proyecto, para este ejemplo usaremos un sitio web estático usando html y css.

## Creando el proyecto

Crearemos una carpeta con los archivos necesarios para nuestro sitio web. Vamos a crear una carpeta con el nombre _web-presentacion_ dentro de la carpeta crearemos las subcarpetas: **css**,**img**, **estilos** y nuestro **index.html**.

Vamos a escribir las siguientes etiquetas para nuestro archivo _index.html_ (Utilizando Visual Studio Code como nuestro editor de texto)

``` html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="estilos/estilos.css">
    <title>Mi presentación</title> 
</head>
<body>
    <div class="contenedor">
        <h1>Bienvenid@s</h1>
        <img src="img/miavatar.png" alt="">
        <p>Mi nombre es <spam>Deploy Web</spam>, desarrollo sitios web modernos usando <i>HTML, CSS y Javascript</i></p>
        <button>Visita mi blog</button>
    </div>
</body>
</html>

```

Recordar que en la carpeta **img** deberas utilizar una imagen representativa.

Resultado:
![Web html]({{ site.baseurl }}/assets/img/posts/html.png)

## Archivo CSS

Vamos a darle un estilo a nuestro sitio web para esto crearemos en la carpeta **estilos** un archivo llamado _estilos.css_ y escribimos lo siguiente:

``` css

html{
    background: #FF416C;  /* fallback for old browsers */
    background: -webkit-linear-gradient(to right, #FF4B2B, #FF416C);  /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to right, #FF4B2B, #FF416C); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    width: 100%;
}
img{
    border-radius: 50%;
    border: white solid 5px;
}

body{
    color: white;
}

h1{
    font-family:'Open Sans';
    font-size: 3em;
    letter-spacing: 5px;
}

p{
    font-family: 'Courier New';
    font-size:1.5em;
    
}
spam{
    font-size:2em;
    font-weight: 500;
}

button{
    background: purple;
    border: white solid 1px;
    border-radius: 75px;
    color: white;
    font-size: 1em;
    height: 50px;
    width: 150px;
}

.contenedor{
    padding: 0 40px 0 40px;
    text-align: center;
}

```

El cual sera mucho mejor el resultado:
![Web html con css]({{ site.baseurl }}/assets/img/posts/html y css.png)

Para generar el degradado he usado el siguiente servicio web (recomendado)

[Generar gradientes css](https://uigradients.com/ "Gradientes css")

## Usar **git**

Para usar git deberemos instalar desde el siguiente enlace:

[https://git-scm.com/](https://git-scm.com/ "Instalar git")

Sigue el asistente y listo. Para comprobar si se encuentra instalado en nuestro PC, abre una terminal en MAC o una ventana de MS-DOS en Windows y teclea lo siguiente y presiona ` Enter `

` git --version `

Mostrará la versión que tienes instalada.

## Github

Ahora es momento que creemos un repositorio para subir nuestro proyecto.

Abre una cuenta nueva en **Github** en el siguiente enlace:

[https://github.com/](https://github.com/ "Cuenta en github)

Una vez registrado, inicias sesión y vamos a crear un repositorio.

![Repositorio en github]({{ site.baseurl }}/assets/img/posts/repositorio.png)

Escribimos un nombre y una descripción para el repositorio y click en _Create Repository_

![Repositorio en github]({{ site.baseurl }}/assets/img/posts/repo.png)

Veremos la siguiente pantalla:

![Código en github]({{ site.baseurl }}/assets/img/posts/code.png)

No cierres la ventana y vamos a abrir nuestro proyecto en _Visual Studio Code_

## Subir el repositorio

Una vez abierto el proyecto nos vamos apoyar en la **terminal integrada** de Visual Studio Code. Si no se encuentra visible click en el menú `Ver-Terminal integrado`

En la terminal escribimos `git init` y presionamos enter 

![Terminal]({{ site.baseurl }}/assets/img/posts/VSC.png)

Ese comando nos permite tener un repositorio local en nuestro PC

Ahora vamos a agregar todos los archivos al repositorio local con el siguiente comando:

`git add .`

El siguiente comando a digitar es para crear nuestro primer **commit** que es básicamente es registrar cambios en el proyecto.

`git commit -m "Primer commit local"`

Ahora vamos a conectar a nuestro repositorio remoto con el siguiente comando:

`git remote add origin https://github.com/jonathanquehay/web-presentacion.git`

Recuerda que debes de copiar la línea que tienes en tú sitio de **github**

![Remoto]({{ site.baseurl }}/assets/img/posts/gitremote.png)

Y para termina y subir los archivos hacia **github** escribe el siguiente comando:

`git push -u origin master`

Listo si ahora actualizas el sitio web del repositorio observaras el proyecto listo en **github**

Nota: Si al momento de escribir el comando observas una ventana es necesario ingresar tus credenciales de **github**.

![Repositorio]({{ site.baseurl }}/assets/img/posts/mi repositorio.png)

Y listo!! 

Espero que logres subir tus repo. :)

Te dejo el link del repositorio creado:

[El repositorio creado](https://github.com/jonathanquehay/web-presentacion)



