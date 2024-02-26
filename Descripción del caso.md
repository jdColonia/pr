![Logo de la Universidad ICESI](https://www.icesi.edu.co/launiversidad/images/La_universidad/logo_icesi.png)
# Informe - Grupo 1

### Participantes ✒️
* Esteban Gaviria Zambrano
* Juan Manuel Díaz Moreno
* Juan David Colonia Aldana
* David Santiago Donneys Taborda
* Carlos Tafurt Burbano

## Estándar de Commit 📌

### Estructura del Mensaje de Commit

Cada mensaje de commit consta de tres partes distintas separadas por una línea en blanco: un título, un cuerpo opcional
y un pie de página opcional. La estructura del mensaje de commit se ve así:

```bash
<tipo>: <título>

<cuerpo (opcional)>

<pie de página (opcional)>
```

### Tipo

Debe ser uno de los siguientes:

- **feat**: Una nueva característica
- **fix**: Una corrección de bug
- **docs**: Cambios en la documentación
- **style**: Cambios que no afectan el significado del código (espacios en blanco, formato, punto y coma perdidos, etc.)
- **refactor**: Un cambio de código que ni arregla un error ni añade una característica
- **perf**: Un cambio de código que mejora el rendimiento
- **test**: Añadir pruebas faltantes o corregir pruebas existentes

### Título

El título contiene una descripción sucinta del cambio. En general, debe ser:

- en minúsculas, con la primera letra en mayúscula
- limitado a 50 caracteres
- comenzar con un verbo en tiempo presente
- no terminar con un punto

### Cuerpo

Al igual que en el título, usa el tiempo presente: "cambia" no "cambiado" ni "cambios". El cuerpo incluye la motivación
para el cambio y contrasta con las implementaciones anteriores.

### Pie de página

El pie de página se utiliza para hacer referencia a las incidencias de seguimiento de problemas.

### Estructura

A continuación, se muestra cómo se ve un mensaje de commit siguiendo esta estructura:

```bash
feat: Resumen de los cambios en alrededor de 50 caracteres o menos

Se proporciona un resumen conciso de los cambios realizados, limitado a unos 72 caracteres aproximadamente. Se enfatiza 
la importancia de la línea en blanco que separa el resumen del cuerpo del mensaje de commit. Esto facilita la 
comprensión por parte de varias herramientas, como log, shortlog y rebase, evitando confusiones.

Se explica detalladamente el problema que este commit aborda, centrándose en el porqué del cambio en lugar del cómo. Se 
alienta a proporcionar información sobre posibles efectos secundarios o consecuencias no intuitivas de la modificación. 
Los párrafos adicionales se presentan después de líneas en blanco, y se aceptan viñetas con una sangría colgante para 
una mejor organización y legibilidad del texto.

Resuelve: #123

Ver también: #456, #789
```

## Guía de Estilos del Código 🗒️

### Indentación

Utilizamos 4 espacios por nivel de indentación.

### Líneas en blanco

Usamos dos líneas en blanco para separar las definiciones de las clases y una línea en blanco para separar las funciones
y los métodos dentro de las clases.

### Importaciones

Las importaciones deben estar en líneas separadas.

### Espacios en blanco

Evitamos los espacios en blanco inmediatamente dentro de los paréntesis, corchetes o llaves.

### Comentarios

Los comentarios deben ser completos y claros.

### Convenciones de nombres

- Los nombres de las clases deben seguir la convención CapWords.
- Los nombres de las funciones y variables deben ser en minúsculas con palabras separadas por guiones bajos.
- Los nombres de las constantes deben estar en mayúsculas con palabras separadas por guiones bajos.

### Longitud de línea

Limitamos todas las líneas a un máximo de 79 caracteres.

### Referencias

Para más detalles, consulte la [Guía de Estilo de Python (PEP 8)](https://recursospython.com/pep8es.pdf).

## Forma de ejecutar el código

Nota: El código se puede ejecutar desde la carpeta "code" utilizando el comando `python Main.py` o desde un IDE.

## Evidencias 📸

### Creación de ramas

<img src="https://i.ibb.co/4jFWLWD/image.png" alt="image" border="0">

### Código realizado

#### Clase Main

<img src="https://i.ibb.co/fxyKRgB/code1.png" alt="code1" border="0">

#### Clase Evento

<img src="https://i.ibb.co/T1Tq3k8/code2.png" alt="code2" border="0">

#### Clase Ponente

<img src="https://i.ibb.co/wMFWW2k/code3.png" alt="code3" border="0">

### Ejecución del código

<img src="https://i.ibb.co/yXjtnmQ/Captura-de-pantalla-2024-02-26-104814.png" alt="Captura-de-pantalla-2024-02-26-104814" border="0">

<img src="https://i.ibb.co/brMq4z6/Captura-de-pantalla-2024-02-26-104842.png" alt="Captura-de-pantalla-2024-02-26-104842" border="0">

<img src="https://i.ibb.co/SJgk9FX/Captura-de-pantalla-2024-02-26-104907.png" alt="Captura-de-pantalla-2024-02-26-104907" border="0">
