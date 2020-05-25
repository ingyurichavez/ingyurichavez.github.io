# CURSO WEBPACK
- Webpack es un empaquetador
- webpack solo entiende js y json por eso instalamos los louders
- tenemos:
    - entry:
        - es el punto, archivo de entrada de la aplicacion (entry: "./src/index.js" por defecto)
        - multi page aplication = es tener varios puntos de entrada
    - output:
        - archivo de salida
        - crea por defecto la carpeta dist y dentro un archivo main.js
    - loaders:
        - son los que transforman codigo
        - ayuda interpretar, reconocer otros archivos
        - se configura en el module: {}
    - plugins:
    - mode:

## ¿que podemos hacer?
- trasnpilar de babel a es5
- crear un servidor web
- podemos dividir los archivos de salida

## Requisitos
- instalar node (incluye npm)

## Comandos principales
> alt + 96 = `
> --save-dev = -D
_iniciar un proyecto nuevo_
    npm init -y
        `crea archivo package.json`
        `-y = a todo le da yes`
        `iniciar un proyecto con npm`
_instalar dependencias de webpack y webpack-cli de manera LOCAL_
    npm i webpack webpack-cli -D
        `instala dependencias solo en tu proyecto`
        `crea carpeta node_modules`
        `crea archivo package-lock.json`
_CSS_
    npm i style-loader css-loader -D
    npm i mini-css-extract-plugin -D
        `extrae el archivo css en un archivo aparte`
_SASS_
    npm i node-sass sass-loader -D
_HTML_
    npm i html-webpack-plugin -D
_Servidor_
    npm i webpack-dev-server -D
_BABEL_
    npm i @babel/core @babel/cli -D
    npm i @babel/preset-env -D
        *babel.config.json*
    npm i core-js
        `esto sirve para los polyfill`
        `si no pongo -D se instala en modo produccion`
        `lista de cosas que necesitan transformar y cosas que necesitan polyfill`
    npm i babel-loader -D
        `traspilar codigo js`
    npm i lodash-es
        `investigar sobre lodash`
_interpretar archivos_ _imagenes, ..._
    npm i file-loader -D

## comandos
_scripts_
    "build": "webpack",
        `crea archivo dist y dentro el archivo de salida`
        `./dist/index.js`
    "start": "webpack-dev-server --open"
        `-d = modo desarrollo`
        `--open = abre el navegador`






_HTML_
    npm i html-webpack-plugin -D
    npm i html-loader -D
    `todo`
    npm i html-webpack-plugin html-loader -D





_postcss y autoprefixer_
    npm i postcss-loader -D
    npm i autoprefixer -D
_limpiar la carpeta dist_
    npm i clean-webpack-plugin -D
_URL_
    npm i resolve-url-loader -D
_PUG_
    npm install pug pug-plain-loader -D


_instalar babel_ *version moderna*
    npm i @babel/core @babel/cli -D
    npm i @babel/preset-env -D
    npm i core-js `modo produccion, para los polyfill`
_crear archivos de configuracion_
 webpack.config.js
 _crear carpeta src y dentro un archivo index.js_

## otros comandos
_instalar dependencias de webpack y webpack-cli de manera GLOBAL_
    npm i webpack webpack-cli -g `instala en toda la pc`
_instalar dependencias babel_ *version antigua*
    npm i -D babel-loader babel-core babel-preset-env
    crear archivo de configuracion .babelrc
        {
            "presets":[
                "env"
            ]
        }
    package.json
        "scripts": {
            "build-babel": "webpack --mode production --module-bind js= "babel-loader",
            "dev-babel": "webpack --mode development--module-bind js= "babel-loader"
        },
    *npm*
    npm run build-babel
    npm run dev-babel
 _Desinstalar dependencias babel_
    npm un -D babel-loader babel-core babel-preset-env
_instalar dependencias babel eligiendo la version_
    npm i -D babel-core@6.26.3
    npm i -D babel-loader@7.1.5
    npm i -D babel-preset_env@1.7.0 `ERROR: no encuentra el servidor`


## Ejemplos
> Ejemplo 1
*package.json*
"scripts": {
    "build": "webpack"
}
*npm*
npm run build `crea la carpeta dist y dentro un archivo main.js`
> Ejemplo 2
*package.json*
`modo produccion (build) y modo desarrollo (dev)`
"scripts": {
    "build": "webpack --mode production",
    "dev": "webpack --mode development"
},
*npm*
npm run build
npm run dev
> Ejemplo 3
_package.json_
`para la entrada: crear carpeta prueba y dentro la carpeta src y dentro el archivo main.js`
`salida: creara una carpeta public y dentro el archivo script.js`
"scripts": {
    "build2": "webpack --mode production ./prueba/dev/main.js --output ./prueba/public/script.js",
    "dev2": "webpack --mode development ./prueba/dev/main.js --output ./prueba/public/script.js"
},
*npm*
npm run build2
npm run dev2


## Comandos
_instalar la dependencia webpack_
    npm i webpack `crea carpeta node_modules y el archivo package-lock.json`
    npm i webpack -g `-g = instala para toda la pc`
    npm i webpack -D `-D = dependencia de desarrollo, los instala solo en tu proyecto`
_instala la dependencia webpack-cli_
    npm i webpack-cli `cli = common line interface`
    npm i webpack-cli -D `instala solo en tu proyecto`



## comandos basicos
_version de npm_
    npm -v
_Version del node_
    node --version
node -v
_limpiar terminal_
    clear
    cls

