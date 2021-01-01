# Curso Intro to Vue3 (https://www.vuemastery.com/courses/intro-to-vue-3)
-------------------------------------------------------------------------

## Lección 1: Intro to Vue3
----------------------------

	Utilización de Visual Studio Code como IDE de desarrollo con el plugin es6-string-html (https://marketplace.visualstudio.com/items?itemName=Tobermory.es6-string-html)


## Lección 2: Creating the Vue App
----------------------------------

	Crear proyecto de prueba (denominado Intro-to-Vue-3)
		mkdir Intro-to-Vue-3

	Crear carpeta assets para albergar las imágenes
		cd Intro-to-Vue-3
		cd assets

    Crear carpeta images y hoja de estilos (Copiar los archivos de https://github.com/Code-Pop/Intro-to-Vue-3/tree/L2-start/assets)
        mkdir images
        Crear archivo styles.css y copiar el contenido del archivo styles.css

    Crear archivos index.html y main.js en la carpeta raiz del proyecto

    index.html: Se importan las hojas de estilos, el archivo de Vue a través del CDN y el archivo main.js

    Crear el siguiente contenido en main.js para crear la aplicación Vue.js

        const app = Vue.createApp({
            data() {
                return {
                    product: 'Socks',
                    // Solution
                    description: 'A warm fuzzy pair of socks.' 
                    // Solution
                }
            }
        })

    Los pasos para montar una aplicación en Vue.js son 

    1. Definir la capa (div) en la que estará nuestra aplicación de Vue3 (index.html)

        <div id="app">
            <h1>{{ product }}</h1>
        </div>

    1. Crear la aplicación Vue.js (main.js)

        const app = Vue.createApp({
            data() {
                return {
                    product: 'Socks',
                    description: 'A warm fuzzy pair of socks.'
                }
            }
        })

    2 . Importar el archivo .js (index.html)

        <script src="./main.js"></script>

    3. Montar la aplicación en el DOM (index.html)
        
        <script>
          const mountedApp = app.mount('#app')
        </script>

    Vue.js es reactivo, lo que significa que los cambios que se produzcan en los datos dentro de {{ }} se renderizan
    automáticamente.

    Añadir a git
        git init
        git add .
        git commit -m "Creating the Vue App"
	    git remote add origin https://github.com/Digitalthink-es/Intro-to-Vue-3.git
	    git push -u origin master