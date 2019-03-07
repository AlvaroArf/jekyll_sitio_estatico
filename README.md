#Sitio web estático con Jekyll
> Para realizar los siguientes pasos, antes debemos de tener Ruby instalado.Para realizar los siguientes pasos, antes debemos de tener Ruby instalado.

##Git Clone - TENGO QUE COMPROBARLO
Si usted quiere llevarse el repositorio a su equipo físico, no necesita mas que tener instalado Ruby y la gema indicada en el primer paso de la instalación

##Instalación
Para comenzar, debemos instalar jekyll en nuestro equipo, para ello instalaremos la siguiente gema

  	$ gem install jekyll bundler

###Creación de sitio web estático
Para crear un nuevo sitio web estático, ejecutamos el siguiente comando en la terminal:

	$ jekyll new misitio

Al ejecutarlo, Jekyll creará un directorio llamado misitio siguiente estructura:
INTRODUCIR IMAGEN 1

Debido a que Jekyll es principalmente un generador de blogs, en el directorio **_posts/** almacenaremos todos los artículos que deben aparecer en orden cronológico
INTRODUCIR IMAGEN 2

####_Config.yml
El archivo _config.yml sirve para editar las configuraciones por defecto de Jekyll. Con él podemos controlar la forma en la que Jekyll debe generar los artículos y las páginas web estáticas.

####Gemfile
El archivo Gemfile permite definir las dependencias o librerías de Ruby adicionales que podamos llegar a necesitar al momento de crear el sitio web.

####Archivos .md
Finalmente, los archivos con extensión .md o .markdown son los que componen el contenido de las páginas y artículos del sitio web estático. Jekyll los transformará a código HTML en el proceso de compilación.

>Adicionalmente, se instalarán algunas librerías adicionales como son el tema minima y una librería para la generación de feeds RSS.

Por último, para generar el sitio introducimos el siguiente comando dentro de la estructura generada anteriormente:

	$ bundle exec jekyll serve

INTRODUCIR IMAGEN 3

###Creación de Artículos
Para agregar artículos al sitio web estático que acabamos de generar, vamos a crear un nuevo archivo en el directorio _posts/ y lo vamos a nombrar teniendo en cuenta el patrón YYYY-MM-DD-nombre-del-archivo.markdown

Ejemplo de contenido:

	---
	layout: post
	title: ¡Bienvenido a Jekyll!
	date: 2019-03-07 10:44:50 -0500 -0500
	---
	Este es el tema básico de Jekyll. Puede encontrar más información acerca de la
	personalización de su tema, así como documentación sobre el uso de Jekyll en
	[jekyllrb.com](http://jekyllrb.com/).

	Puede encontrar el código fuente del tema en: {% include icon-github.html
	username="jekyll" %} / [minima](https://github.com/jekyll/minima)

	Puede encontrar el código fuente de Jekyll en {% include icon-github.html
	username="jekyll" %} / [6](https://github.com/jekyll/jekyll)

INTRODUCIR IMAGEN 5
INTRODUCIR IMAGEN 4

###Agregar páginas al sitio web estático
Para crear una página estática creamos en el directorio raiz un archivo con extensión md

	$ vi acerca.md

Introducimos la siguiente estructura en el archivo y un contenido de ejemplo

	---
	layout: page
	title: Acerca
	permalink: /acerca/
	---
	Este es el tema básico de Jekyll. Puede encontrar más información acerca de la
	personalización de su tema, así como documentación sobre el uso de Jekyll en
	[jekyllrb.com](http://jekyllrb.com/).

	Puede encontrar el código fuente del tema en: {% include icon-github.html
	username="jekyll" %} / [minima](https://github.com/jekyll/minima)

	Puede encontrar el código fuente de Jekyll en {% include icon-github.html
	username="jekyll" %} / [6](https://github.com/jekyll/jekyll)

La variable permalink se utiliza para manipular la URL de la página. En este caso le indicamos a Jekyll que la URL debe ser /acerca/ y no /acerca.html, la cual sería la URL por defecto.

INTRODUCID CAPTURA 6
