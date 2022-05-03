---
layout: post
title: ¿Cómo subir tu código a GitHub?
subtitle: Trucos para subir tu código a GitHub
cover-img: /assets/img/path.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
tags: [GitHub, Git]
---
[github]: https://github.com/
[git]: https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Instalaci%C3%B3n-de-Git
[activada la cuenta de Github mediante un token personal]: https://docs.github.com/es/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token

Mientras aprendes a programar, seguramente te encontrarás muchos ejemplos alojados en [Github][github]{:target="_blank"}. Así que es una buena idea que comiences a subir tus proyectos a dicha plataforma colaborativa, pues te irás acostumbrando a las prácticas de los desarrolladores profesionales.
[Github][github]{:target="_blank"} te permite subir el código fuente, pero también publicarlo como un sitio web (si es que esa es la intención de tu archivo). Esto tienes que tomarlo en cuenta, porque nos puede causar confusión y problemas a la hora de utilizar el control de versiones.

## Requisitos

- Tener una cuenta en [Github][github]{:target="_blank"}
- Tener [activada la cuenta de Github mediante un token personal][activada la cuenta de Github mediante un token personal]{:target="_blank"} en la terminal
- Tener instalado [Git][git]{:target="_blank"}

## Procedimiento

- Ve a tu cuenta de [Github][github]{:target="_blank"} y crea un **nuevo repositorio**. El botón lo encuentras en el lado superior derecho. Ponle el nombre que creas conveniente y da click en el botón verde.

![]({{"/assets/img/subir_proyecto_github/nuevo_repositorio.png"| relative_url}}){: .mx-auto.d-block :}

- Una vez creado, te aparecerá una pantalla con instrucciones, léelas, te servirán para posteriores proyectos. En nuestro caso, sólo necesitamos **copiar la URL de nuestro repositorio**. Tiene la siguiente forma: `https://github.com/yasser-gandhi/jSchatz.git`

- Dirígete a tu terminal y cámbiate a una carpeta recién creada, allí arrastrarás los archivos de tu código. **Te recomiendo que comiences con una carpeta vacía para evitar conflictos de versiones**. Escribe `git init`, esto inicializará el servicio. Después escribe `git clone + la URL de tu repositorio`.

![]({{"/assets/img/subir_proyecto_github/url_git.png"| relative_url}}){: .mx-auto.d-block :}

- Luego escribe `git add .` y posteriormente `git commit -m "Inicio"`. Lo que estás haciendo aquí es agregar los cambios al repositorio y **comentarlo** mediante alguna palabra, en este caso pusimos **Inicio**, pero tú elige la que mejor describa la modificación. Esto te servirá para tener un registro de las versiones que vas subiendo y poder regresar a ellas cuando lo consideres necesario.  

- El siguiente paso es crucial porque tienes que entender cómo vas a subir tu proyecto. Si solo quieres alojar el código escribe `git push origin master`, en cambio, si tu intención es que el servicio te permita publicarlo como sitio web, entonces estás haciendo uso de GitHub Pages, por lo que tendrás que poner `git push origin gh-pages`, aunque previamente tuviste que activar esta característica, pero de eso hablaremos en otro post.     
  Para asegurarte cuál es el **rama** al que tienes que apuntar, ve a la **Sección principal** de tu repositorio y observa cuál es el **branch** seleccionado. Si te equivocas al hacer **push**, simplemente no verás los cambios reflejados porque estarán guardados en otra dirección.

![]({{"/assets/img/subir_proyecto_github/branch-master-gh-pages.png"| relative_url}}){: .mx-auto.d-block :}

- En la terminal verás un mensaje de éxito parecido a esto. Si el proyecto está publicado en **GitHub Pages**, espera unos minutos hasta que se **renderice el sitio**.

![]({{"/assets/img/subir_proyecto_github/exito_github.png"| relative_url}}){: .mx-auto.d-block :}

Y hemos terminado, ahora ya puedes subir tus ejercicios a esta plataforma y compartirlo con tus compañeros y recibir consejos para mejorar tu código. 

# Resumen del código utilizado

~~~
git init
git clone + URL de tu repositorio
git add .
git commit -m "Inicio"
git push origin master
~~~

*!Hasta la próxima!*
