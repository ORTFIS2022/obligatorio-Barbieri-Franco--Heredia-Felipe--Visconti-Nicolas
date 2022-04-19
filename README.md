[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-f059dc9a6f8d3a56e377f745f24479a46679e63a5d9fe6f495e02850cd0d8118.svg)](https://classroom.github.com/online_ide?assignment_repo_id=7412974&assignment_repo_type=AssignmentRepo)

## Profesores

-Alejandro Adorjan

-Johny Kidd


## Integrantes (grupo M4B):

-Franco Barbieri

-Nicolás Visconti

-Felipe Heredia

[Link al repositorio](https://github.com/ORTFIS2022/obligatorio-Barbieri-Franco--Heredia-Felipe--Visconti-Nicolas.git)


# Obligatorio 1:(Título)

## Índice

## Introducción

## Glosario

-NFT: Token no fungible (en inglés: Non Fungible Token). Es un contrato inteligente con tecnología blockchain.
-Blockchain: Estructura de datos cuya información se agrupa en bloques (o conjuntos)

-Ethereum: es un exchange de criptomonedas con tecnología blockchain, que permite la programación de contratos inteligentes (smart contracts) o la creación de tokens, cuya moneda se denomina Ether (ETH).

-Wallet: las Ethereum wallets son aplicaciones que permiten interactuar con las cuentas de ethereum, se usan para ver el balance de la cuenta y hacer transacciones.

-Contratos inteligentes:

-OpenSea

-Repositorio: Espacio centralizado donde se almacena, organiza, mantiene y, quizás, difunde información digital

-Git: herramienta para el versionado de software 

-Marketplace:

-Repositorio: Espacio centralizado donde se almacena, organiza, mantiene y, quizás, difunde información digital
-Git: herramienta para el versionado de software 

-Marketplace:

## Repositorio Git

A continuación vamos a introducir el repositorio en Git, además lo describiremos brevemente.
Utilizar un repositorio en git es útil ya que nos permite trabajar a varias personas en un mismo proyecto, pudiendo modificar el mismo archivo a la vez. Resumidamente, existe un repositorio online en el cual se encuentra la versión "al público" del proyecto, luego cada desarrollador crea un repositorio local en el cual puede traer los datos del repositorio online, hacer cambios, probarlos localmente y combinarlos con los del repositorio online. 
En caso de modificar las mismas líneas del archivo, tendremos que decidir manualmente con cuál opción de la linea nos quedamos.
Para trabajar más prolijamente sin hacer cambios en la versión definitiva del proyecto directamente, pueden utilizarse las ramas, las cuales contienen una copia del repositorio en el momento que son creadas, y donde podemos modificar nuestro software y luego decidir si descartar los cambios o combinar la rama madre con la rama actual para así tener una nueva versión con los cambios realizados.
Nosotros utilizamos principalmente la rama main (princpal) y luego cada uno una rama develop donde hacíamos cambios, luego unimos las ramas una vez los cambios están completos y se van a quedar.


### Creación del repositorio

{cómo fue creado, cómo se agregaron los integrantes, cómo se configuraron permisos, cómo funcionan las ramas, etc.}
El repositorio fue creado utilizando el comando git init y dandole la ruta del del espacio de trabajo colaborativo classroom, 
y luego desde la pagina de github le dimos los permisos de administrador a todos los participantes.


### Comandos utilizados

{Lista con descripción de los comandos y su uso}



## Elicitación

### Investigación: técnicas utilizadas

#### Ingeniería Reversa

La técnica de ingeniería reversa consiste en identificar las funcionalidades de una implementación ya existente de otro sistema similar.
Para identificar algunas de las principales funcionalidades que deben estar presente en nuestro sistema, realizamos esta técnica sobre OpenSea (opeansea.io), el autodenominado marketplace de NFTs más grande.


Pudimos identificar las siguientes funcionalidades:


-Explorar y crear NFTs

-Colecciones de NFTs

-Compra, venta y subasta de NFTs

-Wallet necesaria para poder crear, comprar, vender o subastar los NFTs (no necesaria para explorar)

-Uso de diferentes wallet (MetaMask, Coinbase Wallet, Phantom, etc.)


OpenSea cuenta con más funcionalidades pero creemos que estas son las suficientes y necesarias en términos de nuestro proyecto.


#### Focus Group

#### Análisis de documentación

#### Lluvia de ideas

Para esta técnica cada intengrante propuso 5 ideas sobre el aspecto creativo de proyecto.

##### Ideas de Nicolás:

-Basar la aplicación en NFTs de pinturas. Museo virtual para recorrer colecciones de NFT.

-Los NFTs en la aplicación son exclusivamente contenido multimedia creado por YouTubers/Influencers.

-Sistema de puntos, recompensados mediante algún tipo de juego/minijuego, que se pueden intercambiar por algunos NFTs. Esto no reemplaza la compra/venta de NFTs, es un añadido.

-Red social donde el contenido que se comparte son las NFTs que se pueden comprar en el marketplace de la aplicación.

-Sobres de figuritas, pero de NFTs. Existe la posibilidad de comprar "sobres" de NFTs, los cuales contienen NFTs al azar de determinada colección. Existe un álbum global dentro de la aplicación donde se pueden revisar las "figuritas" NFTs y sus propietarios.


### Referencias bibliográficas

### User Personas

### Modelo conceptual



## Especificación

### Requerimientos funcionales

### Requerimientos no funcionales

#### RNFk: Paleta de colores.

Se indica el nombre del color y el código en hexadecimal.

La paleta de colores primaria de la aplicación será:

-Índigo #3949ab

-Índigo claro #6f74dd

-Índigo oscuro #00227b


La paleta de colores secundaria de la aplicación será:

-Verde #aed581

-Verde claro #e1ffb1

-Verde oscuro #7da453

Para la paleta principal el texto irá en color blanco #ffffff y para la secundaria en negro #000000

#### RNFl: Fuente de texto.

La fuente de texto de la aplicación será Roboto, tamaño 14 por defecto. Para títulos se utilizará tamaño 20 y para subtítulos tamaño 17.

Se utilizará un 100% de opacidad para todos los textos.

#### rnf2 funcionales
-el usuario debe poder comprar ntfs
-el sistema debe solo aceptar ethereum como medio de pago
-el usuario debe poder filtrar el contenido por distintas categorías
-la compra no se debe efectuar si el usuario no cuenta con los fondos necesarios
-el precio definido por el usuario para su nft no puede exceder las 10.000 monedas

#### rnfs
-Al seleccionar un nft se debe visualizar el token precio y una descripción
-la página debe ser adaptativa a cualquier tamaño de pantalla
-los nfts solo pueden ser subidos en formato jpg , png y gif
-la descripción no debe puede exceder los 10.000 caracteres
-el precio no puede exceder las 10.000 monedas


### User Stories

### Use cases

### Boceto de UI



## Validación

## Verificación


## Reflexión

### Detalles del trabajo individual

### Técnicas aplicadas y aprendidas

### Cronograma para reunión (19/4/2022)

-5 ideas c/u en lluvia de ideas 

-Requerimientos funcionales:

Felipe: Requerimientos de wallet

Franco: Requerimientos de compra y venta de NFTs

Nicolás: Requrerimientos de subasta y colecciones de NFTs

-Requirimientos no funcionales:

Felipe: navegador/sistema operativo en el que va a funcionar la aplicación 

Franco: cómo se muestra la info de la NFT

Nicolás: paleta de colores primaria y secundaria, fuente y tamaño

### Cronograma para siguiente reunión (20/4/2022)

Franco: Comandos utilizados

Felipe: User Stories (2)

Nicolás: Requerimientos Funcionales (2) y Requerimientos no funcionales (2)