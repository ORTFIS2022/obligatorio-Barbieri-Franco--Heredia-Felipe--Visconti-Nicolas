# Obligatorio 1: NFTs

[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-f059dc9a6f8d3a56e377f745f24479a46679e63a5d9fe6f495e02850cd0d8118.svg)](https://classroom.github.com/online_ide?assignment_repo_id=7412974&assignment_repo_type=AssignmentRepo)

## Profesores

- Alejandro Adorjan
- Johny Kidd


## Integrantes (grupo M4B):

- Franco Barbieri
- Felipe Heredia
- Nicolás Visconti

[Link al repositorio](https://github.com/ORTFIS2022/obligatorio-Barbieri-Franco--Heredia-Felipe--Visconti-Nicolas.git)


## Índice
1. [Introducción](#introducción)
2. [Conceptos previos](#Conceptos-previos)
    1. [Glosario](#Glosario)
    2. [Supuestos](#Supuestos)
3. [Repositorio Git](#repositorio-git)
    1. [Creación del repositorio](#creación-del-repositorio)
    2. [Comandos utilizados](#comandos-utilizados)
4. [Versionado](#versionado)
    1. [Ramas](#ramas)
    2. [Commits](#commits)
    3. [Evolución del proyecto](#evolución-del-proyecto)
5. [Elicitación](#elicitación)
    1. [Investigación: técnicas utilizadas](#investigación-técnicas-utilizadas)
        1. [Ingeniería Reversa](#ingeniería-reversa)
        2. [Entrevista](#entrevista)
        3. [Lluvia de ideas](#lluvia-de-ideas)
    2. [Referencias bibliográficas](#referencias-bibliográficas)
    3. [User Personas](#user-personas)
    4. [Modelo conceptual](#modelo-conceptual)
6. [Especificación](#especificación)
    1. [Requerimientos funcionales](#requerimientos-funcionales)
    2. [Requerimientos no funcionales](#requerimientos-no-funcionales)
    3. [User Stories](#user-stories)
    4. [Use Cases](#use-cases)
    5. [Boceto de UI](#boceto-de-ui)
7. [Validación](#validación)
8. [Verificación](#verificación)
9. [Reflexión](#reflexión)
    1. [Detalles del trabajo individual](#detalles-del-trabajo-individual)
        1. [Franco](#franco)
        2. [Felipe](#felipe)
        3. [Nicolás](#nicolás)
    2. [Técnicas aplicadas y aprendidas](#técnicas-aplicadas-y-aprendidas)
10. [Anexo](#anexo)

## Introducción

Este documento explica y establece cómo debería ser nuestro software, un marketplace de NFTs, a la hora de implementarlo, se establecen distintos aspectos del mismo como requerimientos funcionales y no funcionales, use cases, user personas, user stories.
Se recomienda el uso del [índice](#índice) para navegar cómodamente por el documento luego de una lectura inicial.

## Conceptos previos

### Glosario
- **NFT**: Token no fungible (en inglés: Non Fungible Token). Es un contrato inteligente con tecnología blockchain.
- **Blockchain**: Estructura de datos cuya información se agrupa en bloques (o conjuntos)
- **Ethereum**: es un exchange de criptomonedas con tecnología blockchain, que permite la programación de contratos inteligentes (smart contracts) o la creación de tokens, cuya moneda se denomina Ether (ETH).
- **Wallet**: las Ethereum wallets son aplicaciones que permiten interactuar con las cuentas de ethereum, se usan para ver el balance de la cuenta y hacer transacciones.
- **Contratos inteligentes**: contrato que se ejecuta por sí mismo sin que intermedien terceros y se escribe como un programa informático en lugar de utilizar un documento impreso con lenguaje legal, estos funcionan con el sistema blockchain.
- **OpenSea**: MarketPlace descentralizado donde se comercializan ntfs
- **Repositorio**: Espacio centralizado donde se almacena, organiza, mantiene y, quizás difunde, información digital.
- **Git**: herramienta para el versionado de software.
- **Marketplace**: Es una plataforma donde se ofrecen determinados productos, a veces se lo conoce como mercado en línea.

### Supuestos
- **Login**: Se asume que el usuario ya tiene un usuario creado en la pagina y esta logueado al mismo.
- **Wallet**: Se asume que el usuario ya tiene asociada una wallet a su cuenta.
- **Menú**: Se asume que no hay que especificar el menú.

## Repositorio Git

A continuación vamos a introducir el repositorio en Git, además lo describiremos brevemente.
Utilizar un repositorio en git es útil ya que nos permite trabajar a varias personas en un mismo proyecto, pudiendo modificar el mismo archivo a la vez. Resumidamente, existe un repositorio online en el cual se encuentra la versión "al público" del proyecto, luego cada desarrollador crea un repositorio local en el cual puede traer los datos del repositorio online, hacer cambios, probarlos localmente y combinarlos con los del repositorio online. 
En caso de modificar las mismas líneas del archivo, tendremos que decidir manualmente con cuál opción de la linea nos quedamos.
Para trabajar más prolijamente sin hacer cambios en la versión definitiva del proyecto directamente, pueden utilizarse las ramas, las cuales contienen una copia del repositorio en el momento que son creadas, y donde podemos modificar nuestro software y luego decidir si descartar los cambios o combinar la rama madre con la rama actual para así tener una nueva versión con los cambios realizados.
Nosotros utilizamos principalmente la rama main (princpal) y luego cada uno una rama develop donde hacíamos cambios, luego unimos las ramas una vez los cambios están completos y se van a quedar.


### Creación del repositorio

El repositorio fue creado utilizando el comando git init y dandole la ruta del del espacio de trabajo colaborativo classroom, 
y luego desde la pagina de github le dimos los permisos de administrador a todos los participantes.
Para crear las ramas dos integrantes la crearon desde github, luego crearon una rama local y le asignaron como origen la rama remota a través del comando **git branch --set-upstream-to=origin/*origenRama* *nombreRama***. El restante integrante la creo directamente desde la terminal. Ambas maneras funcionaron bien.


### Comandos utilizados

Estos son algunos de los comandos más importantes que utlizamos durante del proyecto:
- **git clone *url*:** Clona un repositorio remoto alojado en *url*. además, *url* queda establecido como origen.
- **git branch:** Muestra las ramas, marcando en la que se está trabajando actualmente.
- **git checkout *nombreRama*:** Cambia la rama de trabajo actual a la rama *nombreRama*.
- **git checkout -b *nombreRama*:** Crea una rama con nombre *nombreRama*. Cambia la rama de trabajo actual a la rama *nombreRama*.
- **git status:** Informa el estado (archivos eliminados, agregados, modificados) de la rama actual.
- **git add . :** Agrega todos los archivos para ser utiliados en el próximo commit.
- **git commit -m "*mensaje*":** Establece un punto de control en el desarrolo y guarda los cambios localmente.
- **git push:** "Empuja" los cambios (commits) al servidor remoto. Si hay conflictos, deberán resolverse a través de un nuevo commit.
- **git pull:** Trae el repositorio remoto en su estado actual al repositorio local. Si hay conflictos, deberán resolverse.
- **git merge *nombreRama*:** Combina la rama de trabajo actual con la rama *nombreRama*.
- **git branch --set-upstream-to=origin/*origenRama* *nombreRama*:** Establece el origen de la rama *nombreRama* como origin/*origenRama* donde origin es el origen de la rama main.


## Versionado

### Ramas

Dispusimos de la rama **main** donde se guardan las versiones estables, luego, cada integrante creo su propia rama donde se trabajaban nuevas integraciones al documento en paralelo para luego combinarse al main:
- **develop/Felipe**: rama donde trabajó Felipe
- **developfranco**: rama donde trabajó Franco
- **developNico**: rama donde trabajó Nicolás

{Workflows - Fig. 1}

### Commits

Utilizamos un criterio donde va una descripción de los cambios realizados y al comienzo del commit una palabra que refleja el tipo de  los cambios realizados, a continuación se describen brevemente y se muestran ejemplos:

- **Add**: cuando se agrega un archivo o líneas a un archivo.
    - Ejemplos

    ![Ejemplos Add](/Commits/Ejemplos-Add.png "Ejemplos Add")
    - Figura 2: Ejemplos de prefijo Add 

- **Fix**: cuando se corrige parte de un archivo ya existente, sin agregar cambios nuevos.
    - Ejemplos

    ![Ejemplos Fix](/Commits/Ejemplos-Fix.png "Ejemplos Fix")
    - Figura 3: Ejemplos de prefijo Fix

- **Delete**: cuando se borra un archivo o líneas de un archivo.
    - Ejemplos

    ![Ejemplo Delete](/Commits/Ejemplos-Delete.png "Ejemplo Delete")
    - Figura 4: Ejemplo de prefijo Delete

- **Merge**: cuando se combinan ramas.
    - Ejemplos

    ![Ejemplos Merge](/Commits/Ejemplos-Merge.png "Ejemplos Merge")
    - Figura 5: Ejemplos de prefijo Merge


### Evolución del proyecto

Al comienzo nosotros trabajábamos todos sobre la rama main, sin tener ramas adicionales. Esto en un principio no generó complicaciones, pero una vez se fue haciendo más grande el documento y empezamos a agregar archivos externos, vimos la conveniencia de tener cada uno su rama, así que cada uno creo su propia rama y empezamos a trabajar de esa manera. Esto nos permitió trabajar más ordenadamente y guardar en el main lo que quedábamos en común.

## Elicitación

### Investigación: técnicas utilizadas

#### Ingeniería Reversa

La técnica de ingeniería reversa consiste en identificar las funcionalidades de una implementación ya existente de otro sistema similar.
Para identificar algunas de las principales funcionalidades que deben estar presentes en nuestro sistema, realizamos esta técnica sobre OpenSea (opeansea.io), el autodenominado marketplace de NFTs más grande.


Pudimos identificar las siguientes funcionalidades:


- Explorar y crear NFTs
- Colecciones de NFTs
- Compra, venta y subasta de NFTs
- Wallet necesaria para poder crear, comprar, vender o subastar los NFTs (no necesaria para explorar)
- Uso de diferentes wallet (MetaMask, Coinbase Wallet, Phantom, etc.)


OpenSea cuenta con más funcionalidades pero creemos que estas son las suficientes y necesarias en términos de nuestro proyecto.


#### Entrevista

En esta técnica entrevistamos a un inversor de NFTs, {Nombre Apellido}. Realizamos las siguientes preguntas y obtuvimos sus correspondientes respuestas:

{Preguntas y respuetas}

De esta información pudimos concluir:

{Conclusiones}

#### Lluvia de ideas

Para esta técnica cada intengrante propuso 5 ideas sobre el aspecto creativo del proyecto.

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

##### Ideas de Franco:

- Sugerencias de NFTs que le puedan interesar al usuario en base a  diseños realizados por sus creadores favoritos o dentro de la misma categoría.
- Seguir creadores (buscar creadores).
- Automatizar la compra de un nft en base al precio, (si llega a tal valor, comprar).
- Poder publicar NFTs. 
- Filtrar por precio.
- Permitir al creador del NFT ver el historial de ventas y la opinión de los usuarios de la plataforma.


**Conclusión**: No terminamos tomando explicitamente muchas de las ideas planteadas, pero sí incluímos algunas variaciones de algunas, como el filtrado de NFTs (con precio y otros ítems). Finalmente, terminamos adaptando y transformando algunas de las ideas en ideas nuevas que quedaron en nuestro proyecto, como la fecha de subida y el número de vistas.

### Referencias bibliográficas

- Para los bocetos GUI, se utilizó [Balsamiq](https://balsamiq.com/)
- [Técnicas de priorización](https://librescrum.com/2020/09/22/tecnicas-de-priorizacion/)
- [¿Qué es un User persona?](https://www.questionpro.com/blog/es/que-es-un-user-persona/)
- [User personas](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.1010.835&rep=rep1&type=pdf)

### User Personas


![User persona 1](/userPersonas/userPersona1.PNG "Primer user persona")
- Figura 6: User persona 1.

![User persona 2](/userPersonas/userPersona2.PNG "Segunda user persona")
- Figura 7: User persona 2.

### Modelo conceptual

Para el modelo conceptual del sistema introdujimos las siguientes clases con sus respectivas relaciones:
- **NFT**: contiene toda la información de las NFT.
- **Sistema**: contiene una lista de NFT, de colecciones y de usuarios.
- **Usuario**: contiene los datos de un usuario, una lista de sus NFTs y de sus colecciones de NFT.
    - **Comprador**: Extensión de usuario, cuando tiene uno o más NFTs en su propiedad.
    - **Vendedor**: Extensión de usuario, cuando tiene uno o más NFTs a la venta.

- Modelo
 ![Modelo conceptual del sistema](/UML/modelo_conceptual.png "Modelo conceptual del sistema")
- Figura 8: Modelo conceptual del sistema


## Especificación

### Requerimientos funcionales

Se asignan prioridades con un número entero del 1 al 5, según la siguiente tabla.

| **Número** | **Prioridad** |
| -- | -- |
| 1 | Muy alta |
| 2 | Alta |
| 3 | Media |
| 4 | Baja |
| 5 | Muy baja |

#### RF1: Subasta de NFTs.

**Descripción**: El sistema deberá permitir subastar una NFT, esto es: el propietario debe poder indicar un precio inicial, un precio máximo o la ausencia de precio máximo sobre una de sus NFTs, además de la duración de la subasta. 
Una vez realizado, el propietario puede iniciar la subasta. 

- **Actor**: Propietario/Comprador
- **Prioridad**: 3


#### RF2: Ofertas en subastas.

**Descripción**: El sistema debe guardar todas las ofertas de las subastas. Los potenciales compradores podrán realizar ofertas únicamente más altas que la oferta actual, y esta deberá actualizarse inmediatamente en el sistema si el comprador posee un saldo mayor o igual al precio ofertado por el mismo, en caso contrario, no se realizará la oferta. El saldo indicado para la oferta quedará bloqueado y no se podrá utilizar en otras transacciones.

- **Actor**: Propietario/Comprador
- **Prioridad**: 5

#### RF3: Retiro de ofertas en subastas.

**Descripción**: El sistema deberá permitir retirar una oferta, si el potencial comprador lo indica. Luego se actualiza la lista de ofertas refrescando la oferta más alta.

- **Actor**: Propietario/Comprador
- **Prioridad**: 5

#### RF4: Finalización de la subasta.

**Descripción**: Al cumplirse la duración indicada por el usuario de la subasta, la NFT la adquiere el mejor postor y se resta al saldo de su cuenta lo que ofertó por la NFT.
El saldo de la cuenta del propietario que subastó la NFT se le suma el precio al que fue vendida.

- **Actor**: Propietario/Comprador
- **Prioridad**: 5

#### RF5: Colecciones de NFTs.

**Descripción**: El sistema deberá permitir crear colecciones de NFTs.
El usuario debe indicar el nombre de la colección a ser creada, si ya existiese una colección con ese nombre, no se permitirá crearla.
El usuario puede eliminar una colección, el sistema quitará las NFTs de dicha colección y luego eliminará la colección del sistema.

- **Actor**: Usuario propietario
- **Prioridad**: 4

#### RF6: Agregado y borrado de NFTs a colecciones. 

**Descripción**: El sistema debe permitir que el usuario puede agregar NFTs que le pertenezcan a una colección.
El usuario puede retirar una NFT que le pertenezca de una colección.


- Actor: Usuario propietario
- **Prioridad**: 5

#### RF7: Filtrado de NFTs.
**Descripción**: El sistema debera permitir ordenar NFTs por nombre, precio y popularidad.

- **Actor**: Propietario/Comprador
- **Prioridad**: 5

#### RF8: Wallet.
**Descripción**: El sistema debera permitir al usuario acceder a una wallet.
El sistema debera poder permitir al usuario almacenar las claves para acceder a sus fondos en la blockchain.

- **Actor**: Usuario
- **Prioridad**: 2

#### RF9: Información de NFTs

**Descripción**: El sistema deberá almacenar la información de cada NFT. Esto es: 

1. Una identificación única [(ver RNF3)](#rnf3-identificaciones-únicas-de-nfts)
2. Descripción [(ver RNF4)](#rnf4-descripción-de-una-nft)
3. Precio si está a la venta o en subasta 
4. Propietario actual
5. Colecciones a las que pertenece
6. Contenido multimedia [(ver RNF8)](#rnf8-formato-de-nft)
7. Número de vistas
8. Fecha de subida
9. Rareza [(ver RNF9)](#rnf9-rareza-de-un-nft)

- **Actor**: Sistema
- **Prioridad**: 2

#### RF10: Explorar NFTs.

**Descripción**: El sistema debe permitir explorar NFTs, ordenar por precio decreciente y creciente, por popularidad (número de vistas) decreciente y por fecha de subida más antigua y más nueva.

- **Actor**: Usuario
- **Prioridad**: 2

#### RF11: Compra de NTFs.

**Descripción**: El sistema debe permitir comprar NTFs bajo un precio fijo. La única moneda admitida para la transacción será Ethereum y el sistema debe verificar que el usuario tenga los fondos necesarios para realizar la transacción.

- **Actor**: Comprador
- **Prioridad**: 3

#### RF12: Venta de NTFs.

**Descripción**: El sistema debe permitir la venta de NFTs en la plataforma donde el propietario deberá indicar el precio. El vendedor debe contar con una wallet que funcione con la moneda ethereum.

- **Actor**: Vendedor
- **Prioridad**: 3

#### RF13: Creación de una NFT.

**Descripción**: El sistema debe permitir crear una NFT, esto es, el usuario indicará los puntos 2, 4 y 5 del [Requerimiento funcional RF9](#rf9-información-de-nfts) . El sistema debe almacenar esta información e inicializar los demás puntos en su valor neutral una vez el NFT sea publicado:
- Para su identificación, ver criterio según [RNF3](#rnf3-identificaciones-únicas-de-nfts)
- No se asignará precio.
- No se asignará a ninguna colección.
- Número de vistas en 0.
- Fecha de subida en fecha actual.
- Rareza según criterio descripto en [RNF9](#rnf9-rareza-de-un-nft)

- **Actor**: Usuario/Sistema
- **Prioridad**: 1

#### RF14: Publicación de NTFs.

**Descripción**: El sistema debe permitir la publicación de NFTs en la plataforma. El sistema no publicará un archivo que ya existe en la plataforma.

- **Actor**: Usuario
- **Prioridad**: 3




### Requerimientos no funcionales

#### RNF1: Paleta de colores.

**Descripción**: Se indica el nombre del color y el código en hexadecimal.

La paleta de colores primaria de la aplicación será:

- Índigo #3949ab
- Índigo claro #6f74dd
- Índigo oscuro #00227b


La paleta de colores secundaria de la aplicación será:

- Verde #aed581
- Verde claro #e1ffb1
- Verde oscuro #7da453

Para la paleta principal el texto irá en color blanco #ffffff y para la secundaria en negro #000000

**Prioridad**: 4

#### RNF2: Fuente de texto.

**Descripción**: La fuente de texto de la aplicación será Roboto, tamaño 14 por defecto. Para títulos se utilizará tamaño 20 y para subtítulos tamaño 17.
Se utilizará un 100% de opacidad para todos los textos.

**Prioridad**: 5

#### RNF3: Identificaciones únicas de NFTs

**Descripción**: Las identificaciones de cada NFT serán un número entero.
A la primera NFT se le asigna el número 1.
A cada NFT se le asigna su identificación como el número siguiente a la NFT registrada antes de ella.

**Prioridad**: 1

#### RNF4: Descripción de una NFT

**Descripción**: Las descripciones de las NFT no deberán tener más de 1024 caracteres y no pueden contener los siguientes caracteres: \ , ^

**Prioridad**: 2

#### RNF5: Navegadores compatibles

**Descripción**: La pagina debe correr en las version 100.0.4896.127 de Google Chrome para Windows 10, Linux y MacOs

**Prioridad**: 3

#### RNF6: adaptabilidad en pantalla.

**Descripción**: El sistema funcionará en tamaños de pantalla 1920×1080, 1366×768 y 1280x720.

**Prioridad**: 4

#### RNF7: límite de fijación de precio.

**Descripción**: El precio definido para un nft puede exceder los 10.000 ETH.

**Prioridad**: 5

#### RNF8: Formato de NFT

**Descripción**: Los formatos admitido para el contenido multimedia de una NFT son jpg, png o gif.

**Prioridad**: 2

#### RNF9: Rareza de un NFT

**Descripción**: Los NFT deberán tener un atributo de rareza según el número de propietarios:

- 1-2 propietarios: Rareza Legendaria.
- 2-10 propietarios: Rareza Única.
- 11-25 propietarios: Rareza de élite.
- 26-100 propietarios: Rareza normal.
- 101 o más propietarios: Rareza común.

**Prioridad**: 5

### User Stories

#### RNF10: Nombres de las colecciones

**Descripción**: Los nombres de las colecciones de NFT no pueden exceder los 50 caractéres.

**Prioridad**: 5


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

    - 1.1. El usuario no seleccionó una NFT, vuelvo a paso 1.
    - 3.1. No se indicó un precio válido (palabras en vez de números), vuelvo a paso 3.
    - 5.1. No se indicó un precio válido (palabras en vez de números), vuelvo a paso 5.
    - 7.1. El usuario no indicó un período de tiempo válido, vuelvo a paso 7.
    - 11.1. No hubo ningún postor, se desbloquea la NFT y se mantiene el propietario. Fin de caso de uso.

* **Postcondición**: El mayor postor (o el propietario original si no hubo postores o se retiraron todos los postores) se vuelve propietario de la NFT y se deduce el saldo de su cuenta y se suma a la del propietario original.

* **Bosquejo GUI**

 ![Bosquejo de la interfaz gráfica para subastar una NFT](/BocetosBalsamiq/subasta-vendedor.png "Bosquejo inicial para subastar una NFT")
- Figura 9: Bosquejo de interfaz para subasta de NFT

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

    - 3.1. El usuario indico una oferta menor o igual a la actual. La oferta no se registra y se vuelve al paso 3.
    - 3.2. El usuario indicó una oferta mayor o igual a la oferta máxima. Pasa a 5. Fin de caso de uso.
    - 5.1. No hubo postor o todos se retiraron, no se deduce del saldo de nadie y la transacción no tiene efecto
    - 5.2. El usuario retira la oferta, el sistema actualiza la oferta mayor y desbloquea su saldo.


* **Postcondición**: El mayor postor (o el propietario original si no hubo postores o se retiraron todos los postores) se vuelve propietario de la NFT y se deduce el saldo de su cuenta.

* **Bosquejo GUI**

 ![Bosquejo de la interfaz gráfica para compra en subasta de NFT](/BocetosBalsamiq/subasta-comprador.png "Bosquejo inicial para compra de NFTs en subasta")
 - Figura 10: Bosquejo para compra en subasta de NFT

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

    - 1.1 El nombre ingresado no es válido [(ver RNF10)](#rnf10-nombres-de-las-colecciones). No se crea la colección y se vuelve al paso 1.
    

* **Postcondición**: El sistema ahora contendrá la colección creada por el usuario con las NFTs seleccionadas o no, si se decidió eliminar.

* **Bosquejo GUI**

    * Creación
    ![Bosquejo crear colección](/BocetosBalsamiq/colecci%C3%B3n-crear.png "Bosquejo inicial para crear colección")
    - Figura 11: Bosquejo creación de colección de NFTs

    * Agregar/Eliminar NFT
    ![Bosquejo agregar o quitar una NFT a la colección](/BocetosBalsamiq/colecci%C3%B3n-agregar-quitar.png "Bosquejo inicial para agregar o quitar NFTs")
    - Figura 12: Bosquejo agregar y quitar NFTs a la colección

    * Eliminar colección
    ![Bosquejo eliminar colección](/BocetosBalsamiq/colecci%C3%B3n-eliminar.png "Bosquejo inicial para eliminar colección")
    - Figura 13: Bosquejo eliminar la colección


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

* **Bosquego GUI**

    ![Bosquejo de la interfaz gráfica para Explorar NFTs](/BocetosBalsamiq/ExplorarNFTs-Comprador.png "Bosquejo inicial Explorar NFTs")
    - Figura 14: Bosquejo de interfaz gráfica Explorar NFTs


### UC5: Compra de NFT

Este caso de uso trata sobre el proceso de compra de una NFT del punto de vista de un usuario comprador.

* **Prioridad**: 1
* **Requerimientos asociados**:  [RF9](#rf9-información-de-nfts), [RF8](#rf8-wallet), [RF11](#rf11-compra-de-ntfs)
* **Precondición**: El usuario posee una wallet vinculada.

| **Acción del usuario comprador** | **Respuesta del sistema** |
| ---------------- | ------- |
| 1. El usuario determina una NFT la cual desea comprar | 2. El sistema indica la información asociada a la NFT, definida en [RF9](#rf9-información-de-nfts) |
| 3. El usuario indica que va a comprar la NFT | 4. El sistema bloquea la NFT para que no se use en otras transacciones, deduce el precio del saldo del comprador y lo suma al del vendedor, cambia el propietario al comprador y actualiza la rareza. El sistema ahora desbloquea la NFT. |


* **Cursos alternativos** 

    - 1.1. la NFT no está disponible para venta, vuelvo a caso 1. 
    - 3.1. El usuario comprador no tiene saldo suficiente. El sistema lo informa, fin de caso de uso.

* **Postcondición**: El propietario de la NFT pasa a ser el comprador (si se efectuó la compra correctamente), el saldo del vendedor aumenta y el del comprador disminuye.

* **Bosquejo GUI**

 ![Bosquejo de la interfaz gráfica para compra de NFT](/BocetosBalsamiq/comprar.png "Bosquejo inicial para compra de NFTs")
 - Figura 15: Bosquejo de interfaz gráfica para comprar NFT


### UC6: Venta de NFT

Este caso de uso trata sobre el proceso de venta de una NFT del punto de vista de un usuario comprador.

* **Prioridad**: 1
* **Requerimientos asociados**:  [RF12](#rf12-venta-de-ntfs)
* **Precondición**: El usuario posee al menos una NFT.

| **Acción del usuario vendedorr** | **Respuesta del sistema** |
| ---------------- | ------- |
| 1. El usuario determina una NFT la cual desea vender | 2. El sistema bloquea la NFT para que no sea utilizada en otro proceso de venta o subasta |
| 3. El usuario indica el precio por el que quiere vender la NFT | 4. El sistema almacena dicho precio. |
| 5. El usuario indica que va a vender la NFT | 6. El sistema pone la NFT a la venta |
| - | 7. Se vende la NFT y el sistema deduce el saldo del comprador y se lo suma al usuario vendedor, cambiando el propietario y desbloqueando la NFT | 



* **Cursos alternativos** 

    - 3.1. El precio indicado no es válido [(ver RNF7)](#rnf7-límite-de-fijación-de-precio). El sistema lo informa y vuelve a caso 3.
    - 7.1. El usuario vendedor retira la NFT de la venta. El sistema remueve la transacción y desbloquea la NFT.

* **Postcondición**: El propietario de la NFT pasa a ser el comprador, el saldo del vendedor aumenta y el del comprador disminuye.

* **Bosquejo GUI**

 ![Bosquejo de la interfaz gráfica para venta de NFT](/BocetosBalsamiq/vender.png "Bosquejo inicial para venta de NFTs")
 - Figura 16: Bosquejo de interfaz para venta de NFT

#### UC7: Crear NFT

Este caso de uso trata sobre el proceso de venta de una NFT del punto de vista de un usuario comprador.

* **Prioridad**: 1
* **Requerimientos asociados**:  [RF9](#rf9-información-de-nfts), [RF13](#rf13-creación-de-una-nft), [RF14](#rf14-publicación-de-ntfs)
* **Precondición**: -

| **Acción del usuario vendedorr** | **Respuesta del sistema** |
| ---------------- | ------- |
| 1. El usuario determina crear una NFT | 2. El sistema pide los datos de la NFT |
| 3. El usuario indica el nombre, descripción y sube una imagen para la NFT | 4. El sistema guarda los datos e inicializa una NFT vacía, donde le asigna la id única, el propietario como el usuario, la fecha de subida como fecha actual, sus colecciones en vacío, número de vistas en 0 y el resto de datos como los recibió del usuario. |
| 5. El usuario decide publicar la NFT | 6. El sistema la hace visible para todos los demás |



* **Cursos alternativos** 

    - 3.1. La descripción no es válida [(ver RNF4)](#rnf4-descripción-de-una-nft). El sistema lo informa y vuelve a caso 3.
    - 3.2 La imagen no es válida [(ver RNF8)](#rnf8-formato-de-nft). El sistema lo informa y vuelve a caso 3.
    - 3.3 La imagen ya se encontraba en el sistema como parte de otra NFT. El sistema lo informa y vuelve a caso 3.
    - 3.4 El usuario no ingresa un nombre. El sistema lo informa yu vuelve a caso 3.
    - 5.1 El usuario decide no publicar la NFT. El sistema no hace visible para todos los demás la NFT, Fin de caso de uso

* **Postcondición**: La NFT es publicada visible para los demás usuarios, o no, en el caso del curso alternativo.

* **Bosquejo GUI**

    *  Crear
    ![Bosquejo de la interfaz gráfica para creación de NFTs](/BocetosBalsamiq/crear.png "Bosquejo inicial para crear NFTs")
    - Figura 17: Bosquejo de interfaz de creación de NFTs

    * Publicar
    ![Bosquejo de la interfaz gráfica para publicación de NFTs](/BocetosBalsamiq/publicar.png "Bosquejo inicial para publicar NFTs")
    - Figura 18: Bosquejo de interfaz para publicación de NFTs


### Boceto de UI

Para realizar los bocetos de la interfaz de usuario, utilizamos la herramienta [Balsamiq](https://balsamiq.com/), que está justamente pensada para bocetos de interfaz, en un formato similar a lo que sería un bosquejo en papel, en blanco y negro.
Esta herramienta posee la funcionalidad de poder vincular los bocetos entre sí resultando en un prototipo sencillo.
A continuación se explica cómo probar el prototipo, se deben seguir los siguientes pasos:

* Descargar [Balsamiq](https://balsamiq.com/).

* Descargar el [prototipo](/Prototipo/demo.bmpr).

* Ejecutar Balsamiq.

    ![Imagen Balsamiq](/Explicaci%C3%B3nPrototipo/Balsamiq-Wireframes.png "Balsamiq")

* En la esquina superior izquierda: click en pestaña File > Open Project > Ubicación_del_prototipo.

    ![Imagen abrir proyecto](/Explicaci%C3%B3nPrototipo/Open-Project.png "Abrir proyecto")

* En la esquina superior derecha, apretar el botón para ejecutar la presentación en pantalla completa.

    ![Imagen presentación en pantalla completa](/Explicaci%C3%B3nPrototipo/Full-Screen.png "Presentación en pantalla completa")

* Seleccionar "User test" en el menú de opciones y cerrarlo

    ![Imagen seleccionar User Test](/Explicaci%C3%B3nPrototipo/User-Test.png "Seleccionar User Test")

* El prototipo está listo para ser probado.

    ![Imagen inicio Prototipo](/Explicaci%C3%B3nPrototipo/Inicio.png "Pantalla de inicio del prototipo")


## Validación

Realizamos la validación utilizando el prototipo planteado en [bocetos de UI](#boceto-de-ui), además les mostramos a los usuarios el documento para que se adentrasen más concretamente en el contexto de nuestro software. A continuación se plantea la descripción de usuarios validados, seguida de sus comentarios y una conclusión al respecto.
Se marca con **(+)** si el comentario es positivo, con **(-)** si el comentario es negativo y con **(!)** si el comentario es una sugerencia

### Usuario 1

* **Descripción del usuario**: mujer adulta, profesional de clase media-alta.
* **Comentarios del usuario**
    - El prototipo es user friendly. **(+)**
    - Pocos pasos para cada funcionalidad (se llega rápido a la funcionalidad deseada). **(+)**
    - Indicador de cuántas personas intentan realizar la misma transacción. **(!)**
    - En menú principal: tabla de operaciones frecuentes. **(!)**
* **Conclusiones**
    - El prototipo fue agradable para el usuario, consideró que es rápido y amigable.
    - Agregar un indicador de las personas que están intentando realizar una misma transacción puede ser incitador a intentar realizar la transacción rápida. Creemos que en nuestro caso puede ser más enriquecedor un indicador de cuántas personas estuvieron en la página de subasta/compra en las últimas 24 horas.
    - La tabla de operaciones frecuentes es una muy buena idea que muy posiblemente debiéramos incluir. No todos los usuarios van a realizar as mismas operaciones y por ende puede resultar positivo para la experiencia del usuario, agregándole valor.

### Usuario 2

* **Descripción del usuario**: hombre joven, estudiante de clase media-alta.
* **Comentarios del usuario**
    - El prototipo resulta user friendly. **(+)**
    - No se pueden modificar los valores (los números como el precio son fijos). **(-)**
    - Un prototipo más cercano a la versión final. **(!)**
* **Conclusiones**
    - El prototipo nuevamente fue agradable para el usuario, sin embargo esta vez no gustó que los números fueran fijos y no se pudieran modificar, tal vez en la siguiente iteración sería sensato agregar esto al prototipo, aunque consideramos que no debe ser una prioridad, pero tal vez aporta para el usuario tener un prototipo más cercano a la versión definitiva.


## Verificación

Para la verificación de los requerimientos utilizamos distintas técnicas:

### Revisión de pares

Revisión de pares es una técnica donde los colegas revisan el trabajo de uno. Cuando un integrante realiza un nuevo commit, los demás revisan el contenido agregado y dan un feedback sobre si creen que ya está completo y correcto el aporte, o si creen que hace falta algo o que habría que realizar cambios. Para lo segundo, luego se debe revisar nuevamente tras realizar los cambios. Nosotros utilizamos esta técnica de manera que los otros dos integrantes revisaban el trabajo del que realizó el commit.

En particular esta técnica nos fue especialmente útil para identificar errores pequeños, como lo pueden ser faltas de ortografía, legibilidad de alguna estructura, sintaxis de markdown, etc. Además, nos permitió verificar otro tipo de cosas como los requerimientos, casos de uso, que contuviesen todo lo que tenían que contener y que estuvieran correctos.


### Walkthrough

Walkthrough es una metodología donde el autor da un recorrido sobre una parte del sistema, a través de la interfaz, con el fin principalmente de verificar la usabilidad que tiene esa parte del sistema.

Nosotros utilizamos esta metodología mayormente en la parte de los bocetos de interfaz de usuario, donde tras realizar un boceto, hacíamos un recorrido por el mismo a los demás integrantes del grupo. Si algo pareciera que pudiese mejorarse o corregirse, lo hacíamos en el momento.

### Checklist

Checklist es una técnica en la cual se utiliza una lista que contiene lo que debe estar, y se va **checkeando** lo que está presente en la lista. Si hay algo que no marcamos como **checkeado**, entonces lo que estamos verificando no contiene todo lo que debe contener. Este método nos permite verificar la completitud de nuestro software, es decir, que hace todo lo que debería hacer y que tiene todo lo que debería tener.

Utilizamos las siguientes listas, basadas en las mostradas en clase [(ver en anexo)](#anexo):

* **Para requerimientos**
    * ¿Están correctamente priorizados?
    * ¿Tiene una única interpretación?
    * ¿Se puede probar?
    * ¿Tienen el nivel de detalle adecuado?
    * ¿Están duplicados?
    * ¿Tienen conflictos entre sí?
    * ¿Evita incluir aspectos de diseño?
    * ¿Están al alcance?
    * ¿Se pueden identificar y de forma única?
    * ¿Se referencian entre sí de manera correcta?

* **Para casos de uso**
    * ¿Cumple un único objetivo?
    * ¿Es medible para el usuario?
    * ¿Queda claro qué actor(es) participan?
    * ¿Existe una secuencia lógica en los pasos que permita entender la transacción entre el actor y el sistema?
    * ¿Es el nivel de abstracción el adecuado?
    * ¿Está libre de detalles de diseño e implementaciones?
    * ¿Se documentan todos los casos alternativos?
    * ¿Las pre y postcondiciones son las adecuadas?

Particularmente utilizamos esta técnica para revisar que nuestro documento contenía todo lo que se pedía más específicamente y esto nos permitió tener una manera más formal para verificar requerimientos y casos de uso.

### Tabla Requerimientos Funcionales (RF) vs Casos de uso (UC)

Para verificar que los casos de uso contemplen todos los requerimientos funcionales, utilizamos una tabla donde se marca con **v** si están relacionados.

| - | [UC1](#uc1-subasta-de-nft---vendedor) | [UC2](#uc2-subasta-de-nft---comprador) | [UC3](#uc3-crear-y-agregar-nfts-a-colecciones-de-nft) | [UC4](#uc4-explorar-nfts---comprador) | [UC5](#uc5-compra-de-nft) | [UC6](#uc6-venta-de-nft) | [UC7](#uc7-crear-nft) |
| -- | -- | -- | -- | -- | -- | -- | -- |
| [RF2](#rf2-ofertas-en-subastas)                           | - | v | - | - | - | - | - |
| [RF1](#rf1-subasta-de-nfts)                               | v | - | - | - | - | - | - |
| [RF3](#rf3-retiro-de-ofertas-en-subastas)                 | v | v | - | - | - | - | - |
| [RF4](#rf4-finalización-de-la-subasta)                    | v | v | - | - | - | - | - |
| [RF5](#rf5-colecciones-de-nfts)                           | - | - | v | - | - | - | - |
| [RF6](#rf6-agregado-y-borrado-de-nfts-a-colecciones)      | - | - | v | - | - | - | - |
| [RF7](#rf7-filtrado-de-nfts)                              | - | - | - | v | - | - | - |
| [RF8](#rf8-wallet)                                        | - | - | - | - | v | - | - |
| [RF9](#rf9-información-de-nfts)                           | - | - | - | - | v | - | v |
| [RF10](#rf10-explorar-nfts)                               | - | - | - | v | - | - | - |
| [RF11](#rf11-compra-de-ntfs)                              | - | - | - | - | v | - | - |
| [RF12](#rf12-venta-de-ntfs)                               | - | - | - | - | - | v | - |
| [RF13](#rf13-creación-de-una-nft)                         | - | - | - | - | - | - | v |
| [RF14](#rf14-publicación-de-ntfs)                         | - | - | - | - | - | - | v |

En la tabla se puede observar que todos los requerimientos funcionales están asociados a 1 o más casos de uso, y viceversa, que todos los casos de uso contemplan alguno o más requerimientos funcionales.
Esto significa los casos de uso contemplan todos nuestros requerimientos funcionales, por lo cuál podemos concluir que no nos faltan casos de uso.


## Reflexión

### Detalles del trabajo individual

#### Franco

* **Aportes**
    - Estructura del documento
    - Glosario: Contratos inteligentes, OpenSea
    - Comandos utilizados
    - Requerimientos funcionales 11, 12, 13
    - Requerimients no funcionales 6, 7
    - Lluvia de ideas
    - Entrevista
    - User personas 1 y 2
    - Verificación
    - Validación

* Reflexión

#### Felipe

* **Aportes**
    - Creación del repositorio
    - Estructura del documento
    - Explicación creación del repositorio.
    - Glosario: Ethereum, Wallet
    - Requerimientos funcionales 7, 8
    - Requerimiento no funional 5
    - User stories 3 y 4
    - Use case 4
    - Lluvia de ideas
    - Verificación
    - Validación
    

* **Reflexión**

#### Nicolás

* **Aportes**
    - Estructura del documento
    - Glosario: NFT, Blockchain, Repositorio, Git, Marketplace
    - Repositorio: Introducción.
    - Ingeniería Reversa
    - Lluvia de Ideas
    - Requerimientos funcionales 1, 2, 3, 4, 5, 6, 9, 10, 14
    - Requerimientos no funcionales 1, 2, 3, 4, 8, 9, 10
    - Índice
    - User stories 1 y 2
    - Use cases 1, 2, 3, 5, 6, 7
    - Verificación: explicación Checklist, Revisión de pares, Walkthrough y tabla Requerimientos funcionales vs casos de uso
    - Técnicas aprendidas
    - Modelo conceptual
    - Versionado: commits, ramas y evolución del proyecto
    - Anexo
    - Identificadores de figura
    - Prototipo
    - Verificación
    - Validación: Introducción. Usuarios 1 y 2.
    - Detalles del trabajo individual: aportes de los tres integrantes

* **Reflexión**
    - Considero que aporté positivamente en el trabajo y trabajamos de una manera ordenada, que tal vez al principio nos costó un poco organizarnos pero con el tiempo logramos ordenarnos mejor y trabajar limpiamente, repartiendonos las tareas y verificando el trabajo de los demás mientras hacíamos nuestros aportes.
    - Creo que fuimos un buen equipo y trabajamos eficientemente a lo largo del proyecto, logrando un documento con el que estamos conformes y que según entiendo cumple su función de buena manera. 
    - Salimos del obligatorio con muchas herramientas nuevas, no solo en el área de especificar un documento, también herramientas generales, como las técnicas de priorización, la interacción con un usuario para validar nuestra solución, etc. Como herramientas dentro del área aprendimos a utilizar git y github, que considero va a ser fundamental a la hora de realizar futuros trabajos, así como técnicas de investigación, especificar requerimientos funcionales y no funcionales, casos de uso, user stories, user personas y saber cuándo hay que tener cuidado de no dar detalles de implementación cuando no corresponde.



### Técnicas aplicadas y aprendidas

Durante el obligatorio, aprendimos distintas técnicas que aplicamos a nuestro documento:

* Técnicas de priorización
    * **RICE**: **R**each, **I**mpact, **C**onfidence, **E**ffort. 
        - Asignamos un número a cada variable, y luego (R x I x C) / E nos da un número que a mayor valor, más prioritario. En nuestro caso a mayor valor, menor el número que le asignamos como probabilidad (ya que 1 es el más prioritario y 5 el menos prioritario).
    * **M**o**SC**o**W**: **M**ust, **S**hould, **W**ould, **C**ould.
        - Must: Lo que debemos hacer y vamos a hacer de inmediato.
        - Should: Lo que deberíamos hacer y vamos a hacer en lo posible.
        - Could: Lo que podríamos hacer y vamos a hacer si somos capaces.
        - Would: Lo que no vamos a hacer ahora y tal vez hagamos más tarde.
    * **Pirámide de priorización**: pirámide con las siguientes reglas
        - A mayor altura, más prioridad
        - El nivel que está abajo no puede tener menos escalones que el que está arriba

* Técnicas de verificación
    * [Revisión de pares](#revisión-de-pares)
    * [Walkthrough](#walkthrough)
    * [Checklist](#checklist)

* Técnicas de trabajo en grupo
    * [Repositorio Git](#repositorio-git)
        - Trabajar en distintas ramas y combinarlas
        - Trabajar en un repositorio remoto y local
        - Resolver conflictos

## Anexo

### Cronogramas

Para algunas de las reuniones utilizamos algunos cronogramas:

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

    ### Cronograma para reunión 5 (21/4/2022)

    - Felipe: User Stories: Publicar NFT y subastar NFT

    - Nicolás: armar Índice, User Story: Comprar y vender NFT

    ### Cronograma para reunión 6 (22/4/2022)

    - Franco: formalizar requerimientos (R3)
        - Comandos utilizados (R4)



    - Felipe: Use cases RF 7, 8, 9, 10
        - Ideas de lluvia de Ideas  (R3)



    - Nicolás: Use cases RF 1, 2, 3, 4, 5, 6
        - Avanzar introducción

### Placeholders

Antes de tener la versión definitiva de los bocetos con Balsamiq, se utilizaron placeholders hechos en paint, que se encuentran en la carpeta  ![Placeholders](/Placeholders/)

- Imágenes
    - Placeholder 1: Creación de colecciones

    ![Placeholder 1](/Placeholders/Placeholder-Colecciones-Crear.png)

    * Placeholder 2: Agregar/Eliminar a Colección

    ![Placeholder 1](/Placeholders/Placeholder-Colecciones-Agregar-Eliminar.png "Placeholder Colecciones")

    - Placeholder 3: Eliminar Colección

    ![Placeholder 1](/Placeholders/Placeholder-Colecciones-Eliminar-Coleccion.png "Placeholder Colecciones")

    - Placeholder 4: Subasta - Comprador

    ![Placeholder 1](/Placeholders/Placeholder-Subasta-Comprador.png "Placeholder Subasta")

    - Placeholder 5: Subasta - Vendedor
    
    ![Placeholder 1](/Placeholders/Placeholder-Subasta-Vendedor.png "Placeholder Subasta")

### Checklist

- Checklist de requerimientos y casos de uso mostrada en clase

![Imagen de checklist mostrada en clase](/Anexo/Checklist.png "Checklist mostrada en clase")
