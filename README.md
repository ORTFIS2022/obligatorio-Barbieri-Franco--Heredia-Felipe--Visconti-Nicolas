[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-f059dc9a6f8d3a56e377f745f24479a46679e63a5d9fe6f495e02850cd0d8118.svg)](https://classroom.github.com/online_ide?assignment_repo_id=7412974&assignment_repo_type=AssignmentRepo)

## Profesores

- Alejandro Adorjan
- Johny Kidd


## Integrantes (grupo M4B):

- Franco Barbieri
- Felipe Heredia
- Nicolás Visconti

[Link al repositorio](https://github.com/ORTFIS2022/obligatorio-Barbieri-Franco--Heredia-Felipe--Visconti-Nicolas.git)


# Obligatorio 1: NFTs

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
    2. [Referencias bibliográficas](#referencias-bibliográficas)
    3. [User Personas](#user-personas)
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

Este documento explica y establece cómo debería ser nuestro software, un marketplace de NFTs, a la hora de implementarlo, se establecen distintos aspectos del mismo como requerimientos funcionales y no funcionales, use cases, user personas, user stories.
Se recomienda el uso del [Índice](#índice) para navegar cómodamente por el documento luego de una lectura inicial.

## Glosario

- NFT: Token no fungible (en inglés: Non Fungible Token). Es un contrato inteligente con tecnología blockchain.
- Blockchain: Estructura de datos cuya información se agrupa en bloques (o conjuntos)
- Ethereum: es un exchange de criptomonedas con tecnología blockchain, que permite la programación de contratos inteligentes (smart contracts) o la creación de tokens, cuya moneda se denomina Ether (ETH).
- Wallet: las Ethereum wallets son aplicaciones que permiten interactuar con las cuentas de ethereum, se usan para ver el balance de la cuenta y hacer transacciones.
- Contratos inteligentes:contrato que se ejecuta por sí mismo sin que intermedien terceros y se escribe como un programa informático en lugar de utilizar un documento impreso con lenguaje legal estos funcionan con el sistema blockchain.
- OpenSea: MarketPlace descentralizado donde se comercializan ntfs
- Repositorio: Espacio centralizado donde se almacena, organiza, mantiene y, quizás difunde, información digital.
- Git: herramienta para el versionado de software.
- Marketplace:{Placeholder}

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

Estos son alguno de los comando que utulizamos durante del proyecto:
- git clone: Git clone es un comando para descargarte el código fuente existente desde un repositorio remoto (como Github, por ejemplo).
- git branch: se utiliza para trabajar en paralelo en el mismo proyecto simultaneamente. dentro de la misma se encuentran:
- git checkout para cambiar de una rama a otra
- git status para obtener la informacion sobre la rama actual
- git add: incluye lo cambios en el archivo para el siguiente commit
- git commit: establece un punto de control en el desarrolo y guarda los cambios localmente
- git push: envia los cambios (commits) al servidor remoto
- git pull: recibe las actualizaciones realizadas por los otros integrantes desde el repositorio remoto
- git merge: fusiona la rama acctual con la rama padre.




## Elicitación

### Investigación: técnicas utilizadas

#### Ingeniería Reversa

La técnica de ingeniería reversa consiste en identificar las funcionalidades de una implementación ya existente de otro sistema similar.
Para identificar algunas de las principales funcionalidades que deben estar presente en nuestro sistema, realizamos esta técnica sobre OpenSea (opeansea.io), el autodenominado marketplace de NFTs más grande.


Pudimos identificar las siguientes funcionalidades:


- Explorar y crear NFTs
- Colecciones de NFTs
- Compra, venta y subasta de NFTs
- Wallet necesaria para poder crear, comprar, vender o subastar los NFTs (no necesaria para explorar)
- Uso de diferentes wallet (MetaMask, Coinbase Wallet, Phantom, etc.)


OpenSea cuenta con más funcionalidades pero creemos que estas son las suficientes y necesarias en términos de nuestro proyecto.


#### Focus Group

#### Análisis de documentación

#### Lluvia de ideas

Para esta técnica cada intengrante propuso 5 ideas sobre el aspecto creativo de proyecto.

##### Ideas de Nicolás:

- Basar la aplicación en NFTs de pinturas. Museo virtual para recorrer colecciones de NFT.
- Los NFTs en la aplicación son exclusivamente contenido multimedia creado por YouTubers/Influencers.
- Sistema de puntos, recompensados mediante algún tipo de juego/minijuego, que se pueden intercambiar por algunos NFTs. Esto no reemplaza la compra/venta de NFTs, es un añadido.
- Red social donde el contenido que se comparte son las NFTs que se pueden comprar en el marketplace de la aplicación.
- Sobres de figuritas, pero de NFTs. Existe la posibilidad de comprar "sobres" de NFTs, los cuales contienen NFTs al azar de determinada colección. Existe un álbum global dentro de la aplicación donde se pueden revisar las "figuritas" NFTs y sus propietarios.

##### Ideas de Felipe:

- Crear un logo para la pagina.
- Crear un nombre para la pagina.
- Mostrar la cantidad de NFTs a la venta.
- Crear una funcion de intercambio de NFTs en similar valor.
- Mostrar la cantidad total de valor de una coleccion de un usuario dada por la suma de valores de todos sus NFTs.
- Avisarle al usuario cuando uno de sus NFTs cambie de precio o de propietario.

### Referencias bibliográficas

### User Personas

### Modelo conceptual



## Especificación

### Requerimientos funcionales

Se asignan prioridades con un número entero del 1 al 10, siendo 1 el más prioritario.

#### RF1: Subasta de NFTs.

El sistema deberá permitir subastar una NFT, esto es: el propietario debe poder indicar un precio inicial, un precio máximo o la ausencia de precio máximo sobre una de sus NFTs, además de la duración de la subasta. 
Una vez realizado, el propietario puede iniciar la subasta. 

- Actor: Propietario/Comprador
- Prioridad: 3


#### Rf2: Ofertas en subastas.

El sistema debe guardar todas las ofertas de las subastas. Los potenciales compradores podrán realizar ofertas únicamente más altas que la oferta actual, y esta deberá actualizarse inmediatamente en el sistema si el comprador posee un saldo mayor o igual al precio ofertado por el mismo, en caso contrario, no se realizará la oferta. El saldo indicado para la oferta quedará bloqueado y no se podrá utilizar en otras transacciones.

- Actor: Propietario/Comprador
- Prioridad: 3

#### Rf3: Retiro de ofertas en subastas.

El sistema deberá permitir retirar una oferta, si el potencial comprador lo indica. Luego se actualiza la lista de ofertas refrescando la oferta más alta.

- Actor: Propietario/Comprador
- Prioridad: 3

#### Rf4: Finalización de la subasta.

Al cumplirse la duración indicada por el usuario de la subasta, la NFT la adquiere el mejor postor y se resta al saldo de su cuenta lo que ofertó por la NFT.
El saldo de la cuenta del propietario que subastó la NFT se le suma el precio al que fue vendida.

- Actor: Propietario/Comprador
- Prioridad: 3

#### RF5: Colecciones de NFTs.

El sistema deberá permitir crear colecciones de NFTs.
El usuario debe indicar el nombre de la colección a ser creada, si ya existiese una colección con ese nombre, no se permitirá crearla.
El usuario puede eliminar una colección, el sistema quitará las NFTs de dicha colección y luego eliminará la colección del sistema.

- Actor: Usuario propietario
- Prioridad: 2

#### RF6: Agregado y borrado de NFTs a colecciones. 

El sistema debe permitir que el usuario puede agregar NFTs que le pertenezcan a una colección.
El usuario puede retirar una NFT que le pertenezca de una colección.


- Actor: Usuario propietario
- Prioridad: 2

#### RF7: Filtrado de NFTs.
El sistema debera permitir ordenar NFTs por nombre, precio y popularidad.

- Actor: Propietario/Comprador
- Prioridad: 4

#### RF8: Wallet.
El sistema debera permitir al usuario acceder a una wallet.
El sistema debera poder permitir al usuario almacenar las claves para acceder a sus fondos en la blockchain.

- Actor : Usuario
- Prioridad: 1

#### RF9: Información de NFTs

El sistema deberá almacenar la información de cada NFT. Esto es: 

1. Una identificación única [(ver RNF3)](#rnf3-identificaciones-únicas-de-nfts)
2. Descripción [(ver RNF4)](#rnf4-descripción-de-una-nft)
3. Precio si está a la venta o en subasta 
4. Propietario actual
5. Colecciones a las que pertenece
6. Contenido multimedia (ver RNF{Placeholder})
7. Número de vistas
8. Fecha de subida

- Actor: Sistema
- Prioridad: 1

#### RF10: Explorar NFTs.

El sistema debe permitir explorar NFTs, dicho de otra forma, determinar las NFTs que pueden interesar al usuario (mediante el algoritmo {Placeholder}), ordenar por precio decreciente y creciente, por popularidad (número de vistas) decreciente y por fecha de subida más antigua y más nueva.

- Actor: Usuario
- Prioridad: 2

#### RF11: Compra de NTFs.

El sistema debe permitir comprar NTFs,este puede ser por subasta o compra precio fijo. La única moneda admitida para la transacción será ethereum y el sistema debe verificar que el usuario tenga los fondos necesarios para realizar la transacción.

- Actor: Comprador
- Prioridad: 1

#### RF12: venta de NTFs.
El sistema debe permitir la venta de NFTs en la plataforma,el artículo puede ser ofertado por un precio fijo o en formato de subasta. el vendedor debe contar con una wallet que funcione con la moneda ethereum

Actor: vendedor
Prioridad: 1

#### RF13: Publicación de NTFs.
El sistema debe permitir la publicación de NFTs en la plataforma, este puede ser publicado en formato jpg, png o gif. El sistema no debe permitir la subida de un archivo que ya existe en la plataforma

Actor: Usuario
Prioridad: 1




### Requerimientos no funcionales

#### RNF1: Paleta de colores.

Se indica el nombre del color y el código en hexadecimal.

La paleta de colores primaria de la aplicación será:

- Índigo #3949ab
- Índigo claro #6f74dd
- Índigo oscuro #00227b


La paleta de colores secundaria de la aplicación será:

- Verde #aed581
- Verde claro #e1ffb1
- Verde oscuro #7da453

Para la paleta principal el texto irá en color blanco #ffffff y para la secundaria en negro #000000

#### RNF2: Fuente de texto.

La fuente de texto de la aplicación será Roboto, tamaño 14 por defecto. Para títulos se utilizará tamaño 20 y para subtítulos tamaño 17.
Se utilizará un 100% de opacidad para todos los textos.

#### RNF3: Identificaciones únicas de NFTs

Las identificaciones de cada NFT serán un número entero.
A la primera NFT se le asigna el número 1.
A cada NFT se le asigna su identificación como el número siguiente a la NFT registrada antes de ella.

#### RNF4: Descripción de una NFT

Las descripciones de las NFT no deberán tener más de 1024 caracteres y no pueden contener los siguientes caracteres: \ , ^

#### RNF5: Navegadores compatibles

La pagina debe correr en las version 100.0.4896.127 de Google Chrome para Windows 10, Linux y MacOs


#### RNF8: adaptabilidad en pantalla.
El sistema funcionará en tamaños de pantalla 1920×1080 y 1366×768 .





#### RNF9: límite de fijación de precio.
El precio definido para un nft puede exceder las 10.000 monedas




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


#### US1: Comprar una NFT

- **Como** comprador de NFTs
- **Quiero** comprar una NFT
- **Para** incrementar el valor de mi colección o revenderla

**Criterios de aceptación**

- El comprador debe tener saldo suficiente para realizar la compra


#### US2: Vender una NFT

- **Como** propietario de NFTs
- **Quiero** vender una/s de mis NFT
- **Para** obtener ganancias

**Criterios de aceptación**

- La NFT no puede estar en proceso de subasta/venta

#### US3: Publicacion NFT

- **Como** usuario vendedor 
- **Quiero** publicar una imagen
- **Para**  venderla como NFT

**Criterios de aceptación**

- El vendedor debe subir una imagen en formato png de tamaño 700*700

#### US4: Creacion Subasta NFT

- **Como** usuario vendedor 
- **Quiero** comenzar una subasta
- **Para** vender un NFT obteniendo el mayor beneficio posible

**Criterios de aceptación**

- El vendedor debe tener un NFT en propiedad o publicado por su cuenta



### Use cases

### UC1: Subasta de NFT - Vendedor

Este caso de uso trata sobre el proceso de subasta de una NFT desde el punto de vista de un vendedor, la parte de poner una oferta y vender la NFT.

* **Prioridad**: 5
* **Requerimientos asociados**: [RF1](#rf1-subasta-de-nfts), [RF3](#rf3-retiro-de-ofertas-en-subastas), [RF4](#rf4-finalización-de-la-subasta)
* **Precondición**: El usuario posee al menos una NFT.

| **Acción del usuario vendedor** | **Respuesta del sistema** |
| ---------------- | ------- |
| 1. El usuario determina una NFT de su propiedad que desea vender | 2. El sistema bloquea dicha NFT para que no se pueda utilizar en otra transacción |
| 3. El usuario indica el precio inicial para la oferta | 4. El sistema guarda el precio |
| 5. El usuario indica un precio máximo | 6. El sistema guarda el precio |
| 7. El usuario indica el período de tiempo por el que la NFT estará en subasta | 8. El sistema guarda la información |
| 9. El usuario da comienzo a la subasta | 10. El sistema da de alta la subasta | 
| - | 11. Pasa el tiempo límite y el sistema da de baja la subasta, finalizando la transacción sumando al saldo del propietario la mayor oferta. Se desbloquea la NFT |

* **Cursos alternativos** 

    - 2.1. El usuario no seleccionó una NFT, vuelvo a paso 1.
    - 4.1. No se indicó un precio válido (palabras en vez de números), vuelvo a paso 3.
    - 6.1. No se indicó un precio válido (palabras en vez de números), vuelvo a paso 5.
    - 8.1. El usuario no indicó un período de tiempo válido, vuelvo a paso 7.
    - 11.1. No hubo ningún postor, la transacción no surte efecto y se desbloquea la NFT. Fin de caso de uso.

* **Postcondición**: El mayor postor (o el propietario original si no hubo postores o se retiraron todos los postores) se vuelve propietario de la NFT y se deduce el saldo de su cuenta y se suma a la del propietario original.

* **Bosquejo GUI** {Placeholder}

 ![Bosquejo de la interfaz gráfica para venta de NFT](/Placeholders/Placeholder-Subasta-Vendedor.png "Bosquejo inicial para venta de NFTs")

### UC2: Subasta de NFT - Comprador

Este caso de uso trata sobre el proceso de subasta de una NFT desde el punto de vista de un comprador, la parte de poner una oferta y recibir la NFT en caso de ser el mejor postor.

* **Prioridad**: 5
* **Requerimientos asociados**: [RF2](#rf2-ofertas-en-subastas), [RF3](#rf3-retiro-de-ofertas-en-subastas), [RF4](#rf4-finalización-de-la-subasta)
* **Precondición**: -

| **Acción del usuario comprador** | **Respuesta del sistema** |
| ---------------- | ------- |
| 1. El usuario determina una NFT en subasta por la cual desea ofertar | 2. El sistema indica la mayor oferta actual. |
| 3. El usuario indica una oferta mayor a la actual | 4. El sistema guarda el precio, bloqueando esa cantidad de saldo del usuario para no poder usarse en otra transacción y actualiza la oferta mayor |
|  -  | 5. Finaliza la duración de la subasta y el sistema otorga la NFT al usuario, deduciendo su saldo |


* **Cursos alternativos** 

    - 4.1. El usuario indico una oferta menor o igual a la actual. La oferta no se registra y se vuelve al paso 3.
    - 5.1. No hubo postor o todos se retiraron, no se deduce del saldo de nadie y la transacción no tiene efecto
    - 5.2. El usuario retira la oferta, el sistema actualiza la oferta mayor y desbloquea su saldo.


* **Postcondición**: El mayor postor (o el propietario original si no hubo postores o se retiraron todos los postores) se vuelve propietario de la NFT y se deduce el saldo de su cuenta.

* **Bosquejo GUI** {Placeholder}

 ![Bosquejo de la interfaz gráfica para compra en subasta de NFT](/Placeholders/Placeholder-Subasta-Comprador.png "Bosquejo inicial para compra de NFTs en subasta")

 ### UC3: Crear y agregar NFTs a colecciones de NFT

Este caso de uso trata sobre la creación de colecciones de NFT y agregar/quitar NFTs de la misma. También trata sobre la eliminación de colecciones.

* **Prioridad**: 7
* **Requerimientos asociados**: [RF5](#rf5-colecciones-de-nfts), [RF6](#rf6-agregado-y-borrado-de-nfts-a-colecciones)
* **Precondición**: -

| **Acción del usuario creador de colecciones** | **Respuesta del sistema** |
| ---------------- | ------- |
| 1. El usuario indica el nombre de la colección a crear | 2. El sistema almacena el nombre y crea una colección vacía, se muestra menú con opciones pasos 3, 5, 7 y 9. |
| 3. El usuario indica NFTs a agregar a la colección | 4. El sistema agrega las NFTs seleccionadas a la colección | 
| 5. El usuario indica NFTs que quiera remover de la colección | 6. El sistema elimina las NFTs seleccionadas de la colección |
| 7. El usuario desea eliminar la colección | 8. El sistema desasocia las NFTs de la colección y elimina la colección del sistema |
| 9. El usuario indica finalizar | 10. El sistema sale del menú |


* **Cursos alternativos** 

    - 2.1 El nombre ingresado no es válido (ver RNF{x}). No se crea la colección y se vuelve al paso 1.
    

* **Postcondición**: El sistema ahora contendrá la colección creada por el usuario con las NFTs seleccionadas o no, si se decidió eliminar.

* **Bosquejo GUI** {Placeholder}

    * Creación
    ![Bosquejo crear colección](/Placeholders/Placeholder-Colecciones-Crear.png "Bosquejo inicial para crear colección")
    * Agregar/Eliminar NFT
    ![Bosquejo agregar o quitar una NFT a la colección](/Placeholders/Placeholder-Colecciones-Agregar-Eliminar.png "Bosquejo inicial para agregar o quitar NFTs")
    * Eliminar colección
    ![Bosquejo eliminar colección](/Placeholders/Placeholder-Colecciones-Eliminar-Coleccion.png "Bosquejo inicial para eliminar colección")


### UC4: Explorar NFTs - Comprador

Este caso de uso trata sobre el proceso busqueda de NFTs desde el punto de vista de un comprador.

* **Prioridad**: 6
* **Requerimientos asociados**: [RF7](#rf7-Filtrado-de-NFTs), [RF10](#rf10-Explorar-NFTs)
* **Precondición**: -

| **Acción del usuario comprador** | **Respuesta del sistema** |
| ---------------- | ------- |
| 1. El usuario selecciona la opcion de explorar el mercado de NFTs | 2. El sistema despliega en forma de galeria las miniaturas de los NFTs a la venta ordenados por popularidad. |
| 3. El usuario indica si desea filtrarlos por fecha de publicacion o precio o mantener el filtro en popularidad | 4. El sistema cambia el orden en el que se muestran las imagenes dependiendo del criterio elegido por el usuario|


* **Postcondición**: La pagina debe quedar en forma de galeria para que el usuario pueda hacer click en alguna de las miniaturas y acceder a la pagina de dicho NFT para ver su informacion.

### Boceto de UI



## Validación

## Verificación


## Reflexión

### Detalles del trabajo individual

### Técnicas aplicadas y aprendidas

## Anexo

### Cronograma para reunión 3 (19/4/2022)

- 5 ideas c/u en lluvia de ideas 

- Requerimientos funcionales:

    - Felipe: Requerimientos de wallet
    - Franco: Requerimientos de compra y venta de NFTs
    - Nicolás: Requrerimientos de subasta y colecciones de NFTs

- Requirimientos no funcionales:

    - Felipe: navegador/sistema operativo en el que va a funcionar la aplicación 
    - Franco: cómo se muestra la info de la NFT
    - Nicolás: paleta de colores primaria y secundaria, fuente y tamaño

### Cronograma para reunión 4 (20/4/2022)

- Franco: Comandos utilizados

- Felipe: User Stories (2)

- Nicolás: Requerimientos Funcionales (2) y Requerimientos no funcionales (2)

### Cronograma para siguiente reunión (21/4/2022)

- Felipe: User Stories: Publicar NFT y subastar NFT

- Nicolás: armar Índice, User Story: Comprar y vender NFT

### Cronograma para siguiente reunión (22/4/2022)

- Franco: formalizar requerimientos (R3)
    - Comandos utilizados (R4)



- Felipe: Use cases RF 7, 8, 9, 10
    - Ideas de lluvia de Ideas  (R3)



- Nicolás: Use cases RF 1, 2, 3, 4, 5, 6
    - Avanzar introducción

