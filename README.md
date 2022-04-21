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
1. [Introducción](#introducción)
2. [Glosasrio](#glosario)
3. [Repositorio Git](#repositorio-git)
    1. [Creación del repositorio](#creación-del-repositorio)
    2. [Comandos utilizados](#comandos-utilizados)
4. [Elicitación](#elicitación)
    1. [Investigación: técnicas utilizadas](#investigación-técnicas-utilizadas)
        1. [Ingeniería Reversa](#ingeniería-reversa)
        2. [Focus Group](#focus-group)
        3. [Análisis de documentación](#análisis-de-documentación)
        4. [Lluvia de ideas](#lluvia-de-ideas)
        5. [Referencias bibliográficas](#referencias-bibliográficas)
        6. [User Personas](#user-personas)
5. [Especificación](#especificación)
    1. [Requerimientos funcionales](#requerimientos-funcionales)
    2. [Requerimientos no funcionales](#requerimientos-no-funcionales)
    3. [User Stories](#user-stories)
    4. [Use Cases](#use-cases)
    5. [Boceto de UI](#boceto-de-ui)
6. [Validación](#validación)
7. [Verificación](#verificación)
8. [Reflexión](#reflexión)
    1. [Detalles del trabajo individual](#detalles-del-trabajo-individual)
    2. [Técnicas aplicadas y aprendidas](#técnicas-aplicadas-y-aprendidas)
9. [Anexo](#anexo)

## Introducción

## Glosario

-NFT: Token no fungible (en inglés: Non Fungible Token). Es un contrato inteligente con tecnología blockchain.

-Blockchain: Estructura de datos cuya información se agrupa en bloques (o conjuntos)

-Ethereum: es un exchange de criptomonedas con tecnología blockchain, que permite la programación de contratos inteligentes (smart contracts) o la creación de tokens, cuya moneda se denomina Ether (ETH).

-Wallet: las Ethereum wallets son aplicaciones que permiten interactuar con las cuentas de ethereum, se usan para ver el balance de la cuenta y hacer transacciones.

-Contratos inteligentes:

-OpenSea:

-Repositorio: Espacio centralizado donde se almacena, organiza, mantiene y, quizás difunde, información digital.

-Git: herramienta para el versionado de software.

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
Se asignan prioridades con un número entero del 1 al 10, siendo 1 el más prioritario.

#### RF1: Subasta de NFTs.

El sistema deberá permitir subastar una NFT, esto es: el propietario debe poder indicar un precio inicial, un precio máximo o la ausencia de precio máximo sobre una de sus NFTs, además de la duración de la subasta. 
Una vez realizado, el propietario puede iniciar la subasta. 

-Actor: Propietario/Comprador

-Prioridad: 3


#### Rf2: Ofertas en subastas.

El sistema debe guardar todas las ofertas de las subastas. Los potenciales compradores podrán realizar ofertas únicamente más altas que la oferta actual, y esta deberá actualizarse inmediatamente en el sistema si el comprador posee un saldo mayor o igual al precio ofertado por el mismo, en caso contrario, no se realizará la oferta. El saldo indicado para la oferta quedará bloqueado y no se podrá utilizar en otras transacciones.

-Actor: Propietario/Comprador

-Prioridad: 3

#### Rf3: Retiro de ofertas en subastas.

El sistema deberá permitir retirar una oferta, si el potencial comprador lo indica. Luego se actualiza la lista de ofertas refrescando la oferta más alta.

-Actor: Propietario/Comprador

-Prioridad: 3

#### Rf4: Finalización de la subasta.

Al cumplirse la duración indicada por el usuario de la subasta, la NFT la adquiere el mejor postor y se resta el saldo de su cuenta.

-Actor: Propietario/Comprador

-Prioridad: 3

#### RF5: Colecciones de NFTs.

El sistema deberá permitir crear colecciones de NFTs.
El usuario debe indicar el nombre de la colección a ser creada, si ya existiese una colección con ese nombre, no se permitirá crearla.
El usuario puede eliminar una colección, el sistema quitará las NFTs de dicha colección y luego eliminará la colección del sistema.

-Actor: Usuario propietario

-Prioridad: 2

#### RF6: Agregado y borrado de NFTs a colecciones. 

El sistema debe permitir que el usuario puede agregar NFTs que le pertenezcan a una colección.
El usuario puede retirar una NFT que le pertenezca de una colección.


-Actor: Usuario propietario

-Prioridad: 2

#### RF7: Filtrado de NFTs.
El sistema debera permitir ordenar NFTs por nombre, precio y popularidad.

-Actor: Propietario/Comprador

-Prioridad: 4

#### RF8: Wallet.
El sistema debera permitir al usuario acceder a una wallet.
El sistema debera poder permitir al usuario almacenar las claves para acceder a sus fondos en la blockchain.

-Actor : Usuario

-Prioridad: 1

#### RF9: Información de NFTs

El sistema deberá almacenar la información de cada NFT. Esto es: 

-Una identificación única (ver RNF#X)
-Descripción (ver RNF#X)
-Precio si está a la venta o en subasta 
-Propietario actual
-Colecciones a las que pertenece
-Contenido multimedia (ver RNF#X)
-Número de vistas
-Fecha de subida

-Actor: Sistema

-Prioridad: 1

#### RF10: Explorar NFTs.

El sistema debe permitir explorar NFTs, dicho de otra forma, determinar las NFTs que pueden interesar al usuario (mediante el algoritmo #X), ordenar por precio decreciente y creciente, por popularidad (número de vistas) decreciente y por fecha de subida más antigua y más nueva.

-Actor: Usuario

-Prioridad: 2



### Requerimientos no funcionales

#### RNF1: Paleta de colores.

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

#### RNF2: Fuente de texto.

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

#### RNFx: Identificaciones únicas de NFTs

Las identificaciones de cada NFT serán un número entero.
A la primera NFT se le asigna el número 1.
A cada NFT se le asigna su identificación como el número siguiente a la NFT registrada antes de ella.

#### RNFy: Descripción de una NFT

Las descripciones de las NFT no deberán tener más de 1024 caracteres y no pueden contener los siguientes caracteres: \, ^

### User Stories

### Use cases

### Boceto de UI



## Validación

## Verificación


## Reflexión

### Detalles del trabajo individual

### Técnicas aplicadas y aprendidas

## Anexo

### Cronograma para reunión 3 (19/4/2022)

-5 ideas c/u en lluvia de ideas 

-Requerimientos funcionales:

Felipe: Requerimientos de wallet

Franco: Requerimientos de compra y venta de NFTs

Nicolás: Requrerimientos de subasta y colecciones de NFTs

-Requirimientos no funcionales:

Felipe: navegador/sistema operativo en el que va a funcionar la aplicación 

Franco: cómo se muestra la info de la NFT

Nicolás: paleta de colores primaria y secundaria, fuente y tamaño

### Cronograma para reunión 4 (20/4/2022)

Franco: Comandos utilizados

Felipe: User Stories (2)

Nicolás: Requerimientos Funcionales (2) y Requerimientos no funcionales (2)

### Cronograma para siguiente reunión (21/4/2022)

Felipe: User Stories: Publicar NFT y subastar NFT

Nicolás: armar Índice, User Story: Comprar y vender NFT