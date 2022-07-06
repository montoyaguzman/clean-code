# Clean code

## 1. [Principios generales](#principios-generales)
### 1.1 [Código duplicado](#codigo-duplicado)
### 1.2 [Código qué no se utiliza](#código-qué-no-se-utiliza)
### 1.3 [reutilización de código](#reutilizacion-de-codigo)
### 1.4 [asincronia](#asincronia)
### 1.5 [concurrencia](#concurrencia)

## 2. [Variables](#variables)
### 2.1 [Definición](#variables-definición)
### 2.2 [Inicialización](#inicialización)
### 2.3 [Default values](#valor-por-defecto)
## 3. [Funciones](#funciones)
### 3.2 [Definición](#funciones-definición)
### 3.3 [Inicialización](#inicialización)
### 3.4 [Parámetros](#parámetros)
### 3.5 [destruturing](#concurrencia)
### 3.6 [Un nivel de abstracion](#un-nivel-de-abstracción)
### 3.7 [Funciones puras (side effects)](#funciones-puras-(side-effects))
### 3.8 [encapsule conditions](#encapsule-conditions)
### 3.9 [functional sobre imperativo](#concurrencia)
Scope](#concurrencia)
### 3.10 [orden de las declaraciones](#concurrencia)





Uso correcto de var, let y const
Formateo, Identación y lint
Condicionales
evita condiciones negativas
evita el uso de condicionales switch => polimorfismo
validacion de valores null, undefined, vacío (0 y emptyString), NaN, etc.
Uso de JSON
validate info in json (encadenamiento opcional)
Uso de dummyes.
Uso de constantes.
Instalación de dependencias.
Clases.
dont overwrite generic prototypes, use a class and extends
composicion sobre herencia
usar getters y setters
miembros privados
classes es6
Traducciones.
Manejo de errores.
Documentación.
Comentarios
Docs
Principios de diseño.
SOLID, 
DIP, 
DIY
kiss
yagne
Patrones de diseño
Testing

## Codigo duplicado
contenido de codigo duplicado

## Código qué no se utiliza
contenido de codigo que no se utiliza

## Variables definición
Culaquier definición debe ser inicializada en el valor natural por defecto
```javascript
// string
const fullName = '';
// number
const userAge = 0;
```

## Funciones definición
contenido de codigo que no se utiliza



















Nombres de variables
Nombrado 100% inglés

Usar nombres que sean identificables y buscables dentro del código fuente. Considere seguir las siguientes reglas:

Nombres de variables que hagan relación con su objetivo.


No usar abreviaturas no descriptivas.


Distinciones de significado sin agregar pronombres innecesarios.


Evitar que los nombres contengan información técnica.


Nombrado de acuerdo al tipo de dato.





Usar nombres fáciles de buscar.


Evitar nombres que generen pensar en la funcionalidad que tienen.
    

No repetir contexto innecesario dentro de las propiedades.
    
    




Nombrado de funciones
Las funciones debes realizar una sóla cosa.


Usar nombres largos y descriptivos.










Uso de funciones puras, es decir, crear funciones que no modifique directamente los datos.
    

Organizar la declaración de funciones. Primero se crea la función y luego se ejecuta.



Var, let y const
Usar correctamente la definición de variables según el alcance que se requiera.


Identación y linteo.
Configurar es-lint y formateadores de texto de acuerdo a las sugerencias del global devtools.






Comparaciones de valores undefined, null, “”, 0 o [].
Para comparar los valores mencionados anteriormente, considere:






























Uso de dummyes.
Crear un archivo(s) de dummyes para datos no útiles para el aplicativo. Se sabe que un valor es un dummy cuando tiene uno o más de los siguientes propósitos:
Es información de prueba.
Es un mock de datos para simular la respuesta de un servicio.
















Uso de constantes.
considerar el numero de veces que se use
Crear un archivo de constantes para datos en duro. Se sabe que un valor es constante cuando tiene uno o más de los siguientes propósitos:
No es un dummy.
Es un valor que nunca cambiará en el flujo de un sistema.
Es un valor que se utlizá para mostrar un mensaje o hacer una comparación específica.


Reutilización.
Revisar los componentes AaccCorePage (Cells) y AaccUtils (LitElement).
Usar archivos útiles con funciones genéricas para el proyecto.
Tener al menos un archivo de dummyes y uno de constantes.

Instalación de dependencias.
Todo componente debe estar instalado por una dependencia.
No debe haber componentes de terceros que no estén autorizados por el Release Manager o el Tech Lead Development.

Documentación.
Siguiendo los principios anteriores, el código debe ser entendible, con nombres apropiados y auto documentable. De ser así, en su mayoria no requiere documentación. No obstante, en la práctica suceden circunstancias especiales donde se requiere realizar algo que puede considerarse mala práctica de código y es crucial documentar la razón exacta por la que esto se realizó de esa manera. A continuación se detallan algunas razones generales:
Es necesario implementar o sobreescribir un componente para cumplir con una feature de negocio y no existia otra alternativa.
Se tuvo que hacer código no apropiado para resolver una issue del lenguaje, herramientas o componentes.
Se tiene que duplicar código, archivos o componentes por cuidar la no afectación productiva o facilidad de mantenimiento futuro (validar con release manager o tech lead).
No es posible seguir la buena práctica por necesidad del negocio.


