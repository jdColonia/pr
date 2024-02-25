![Logo de la Universidad ICESI](https://www.icesi.edu.co/launiversidad/images/La_universidad/logo_icesi.png)
# Informe - Grupo 1

### **Participantes** ✒️
* Esteban Gaviria Zambrano
* Juan Manuel Díaz Moreno
* Juan David Colonia Aldana
* David Santiago Donneys Taborda
* Carlos Tafurt Burbano

## Estándar de Commit

### Estructura del Mensaje de Commit

Cada mensaje de commit consta de tres partes distintas separadas por una línea en blanco: un título, un cuerpo opcional
y un pie de página opcional. La estructura del mensaje de commit se ve así:

```
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
- **chore**: Cambios en el proceso de construcción o herramientas auxiliares y bibliotecas

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

```
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

## Guía de Estilos del Código

### Indentación

Utilizamos 4 espacios por nivel de indentación.

### Líneas en blanco

Usamos dos líneas en blanco para separar las definiciones de las clases y una línea en blanco para separar las funciones
y los métodos dentro de las clases.

### Importaciones

Las importaciones deben estar en líneas separadas y al principio del archivo después de cualquier comentario o docstring
del módulo.

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

Para más detalles, consulte la Guía de Estilo de Python (PEP 8).

## Evidencias
