# Caso de estudio: _**FútbolProPredictor: Herramienta de Estadísticas y Pronósticos Futbolísticos**_

## Descripción:

En el ámbito deportivo, las apuestas representan una actividad común y fascinante. No obstante, prever los resultados de
un partido o evento deportivo puede ser un reto, dada la multitud de variables y factores en juego. Con el propósito de
simplificar el análisis para posibles apuestas en partidos de fútbol de ligas nacionales alrededor del mundo, hemos
decidido desarrollar una aplicación dedicada al análisis y pronóstico de estos eventos. Esta herramienta permitirá a los
usuarios acceder a información relevante almacenada en una base de datos relacional, analizarla y aplicarla en la
predicción y apuestas de partidos de fútbol de sus ligas favoritas. Así, los usuarios podrán tomar decisiones informadas
respaldadas por datos y estadísticas en sus apuestas, con el objetivo de obtener los mejores resultados.

La aplicación proporcionará a los usuarios un conjunto amplio de estadísticas, tanto generales como detalladas, que
incluyen victorias, derrotas, empates, partidos jugados, puntos totales, goles, córners, y tarjetas obtenidas por los
equipos hasta un punto específico de la temporada. Además, la aplicación contará con una serie de consultas que
proporcionarán al usuario una estimación de ciertas estadísticas de los próximos partidos, como tarjetas, córners y
goles. Las entidades identificadas para llevar a cabo este proyecto son “Partido”, “Usuario”, “Equipo”, “Liga”,
“Árbitro” y “Estadísticas”, cada una con su propio conjunto de atributos que contribuyen a la diversidad de los datos y
consultas disponibles para el análisis. Esta diversidad de datos permitirá a los usuarios realizar un análisis más
profundo y preciso, mejorando así la calidad de sus decisiones de apuestas.

> [!IMPORTANT]
> La concepción de nuestra aplicación, “FútbolProPredictor”, se sitúa en un equilibrio entre la originalidad y
> la adaptación. Nos inspiramos en plataformas reconocidas como "[OneFootball](https://onefootball.com/es/inicio)" y
> "[FlashScore](https://www.flashscore.co/)" para la recopilación de estadísticas de equipos.
> Sin embargo, sentimos que había espacio para más. Por lo tanto, decidimos añadir un componente de predicción para los
> próximos partidos, basándonos en fórmulas de cálculo de estadísticas disponibles en recursos públicos, como los videos
> de "[El Capi](https://www.youtube.com/@elcapi_sports)" en YouTube. Por esta razón, no consideramos nuestra idea como
> completamente original o adaptada, sino como una combinación innovadora de ambas.

## Objetivos

El objetivo de la aplicación "FútbolProPredictor" es proporcionar a los usuarios una plataforma integral para el
análisis y pronóstico de resultados en partidos de fútbol de ligas específicas. Con este fin, se establecen los
siguientes objetivos:

1. **Análisis detallado:** La aplicación se encargará de recopilar estadísticas relevantes acerca de los equipos,
   árbitros y otros factores determinantes en los encuentros futbolísticos. Este análisis comprenderá datos como
   victorias, derrotas, empates, puntos acumulados, cantidad de goles, córners y tarjetas obtenidas por los equipos
   hasta un momento específico de la temporada.

2. **Predicción de resultados:** Basándose en la información recopilada, la aplicación utilizará fórmulas estadísticas
   para proyectar los resultados futuros de los partidos en términos de tarjetas, córners y goles.

3. **Mejora de la experiencia de apuestas deportivas:** El objetivo último es enriquecer la experiencia de los usuarios
   en el ámbito de las apuestas deportivas al proporcionarles información detallada y pronósticos confiables. Esto
   permitirá que los usuarios tomen decisiones más fundamentadas al realizar sus apuestas, incrementando así sus
   posibilidades de éxito.

## Entidades y relaciones

### Entidades

**Usuario (FUERTE):**
> - ID del usuario
> - Nombre
> - Fecha de registro
> - Liga de preferencia

**Equipo (FUERTE):**
> - ID del equipo
> - ID de la liga
> - Nombre del equipo
> - Estadio

**Liga (FUERTE):**
> - ID de la liga
> - Nombre de la liga
> - País
> - Número de equipos

**Árbitro (FUERTE):**
> - ID del árbitro
> - ID de la liga
> - Nombre del árbitro
> - Promedio de tarjetas amarillas
> - Promedio de tarjetas rojas

**Partido (DÉBIL):**
> - ID del partido
> - Fecha del partido
> - ID equipo local
> - ID equipo visitante
> - ID del árbitro
> - Promedio de goles esperados
> - Promedio de córners esperados
> - Promedio de tarjetas esperadas

**Estadísticas (DÉBIL):**
> - ID del equipo
> - Partidos jugados
> - Victorias
> - Derrotas
> - Empates
> - Puntos totales en la temporada
> - Goles anotados
> - Córners a favor
> - Córners en contra
> - Tarjetas a favor
> - Tarjetas en contra

### Relaciones

1. **Usuario - Liga**
    - **Descripción:** Un usuario tiene una liga de preferencia, y una liga puede tener muchos usuarios. Por lo tanto,
      existe una relación de uno a muchos entre la Liga y el Usuario.
2. **Equipo - Liga**
    - **Descripción:** Un equipo pertenece a una liga, y una liga puede tener varios equipos. Por lo tanto, existe una
      relación de uno a muchos entre la Liga y el Equipo.
3. **Árbitro - Liga**
    - **Descripción:** Un árbitro arbitra en una liga, y una liga puede tener varios árbitros. Por lo tanto, existe una
      relación de uno a muchos entre la Liga y el Árbitro.
4. **Partido - Equipo**
    - **Descripción:** Un partido implica a dos equipos (local y visitante). Por lo tanto, existe una relación de muchos
      a muchos entre el Partido y el Equipo.
5. **Partido - Árbitro**
    - **Descripción:** Un partido es arbitrado por un árbitro. Por lo tanto, existe una relación de uno a uno entre el
      Partido y el Árbitro.
6. **Estadísticas - Equipo**
    - **Descripción:** Las estadísticas están asociadas a un equipo. Por lo tanto, existe una relación de uno a uno
      entre las Estadísticas y el Equipo.

## Reportes de Interés

1. **Promedio de Tarjetas a Favor y en Contra**
    - **Descripción:** Este reporte calcula el promedio de tarjetas amarillas y rojas recibidas y concedidas por los
      equipos. Es útil para evaluar el comportamiento disciplinario de los equipos y su impacto en el juego.
    - **Datos del Informe:** Nombre del equipo, Liga del equipo, Promedio de tarjetas amarillas recibidas, Promedio de
      tarjetas amarillas concedidas, Promedio de tarjetas rojas recibidas, Promedio de tarjetas rojas concedidas.

2. **Equipos con Más Victorias**
    - **Descripción:** Este reporte identifica los equipos con el mayor número de victorias, proporcionando una visión
      clara de los equipos más exitosos en términos de resultados.
    - **Datos del Informe:** Nombre del equipo, Liga del equipo, Número de victorias.

3. **Partidos con Más Goles Esperados**
    - **Descripción:** Este reporte destaca los partidos con la mayor expectativa de goles, basándose en el promedio de
      goles esperados de los equipos participantes. Ayuda a identificar los encuentros más emocionantes en términos de
      potencial de puntuación.
    - **Datos del Informe:** Fecha del partido, Equipos involucrados, Promedio de goles esperados.

4. **Árbitros con Más Tarjetas**
    - **Descripción:** Este reporte identifica a los árbitros que han mostrado más tarjetas amarillas y rojas. Es útil
      para evaluar el estilo de arbitraje y su impacto en el desarrollo del juego.
    - **Datos del Informe:** Nombre del árbitro, Liga que arbitra, Promedio de tarjetas amarillas mostradas, Promedio de
      tarjetas rojas mostradas.

5. **Partidos con Menos Tarjetas Esperadas**
    - **Descripción:** Este reporte destaca los partidos con la menor expectativa de tarjetas amarillas y rojas,
      basándose en el promedio de tarjetas esperadas de los equipos participantes. Puede ser relevante para aquellos
      interesados en partidos con menor tensión disciplinaria.
    - **Datos del Informe:** Fecha del partido, Equipos involucrados, Promedio de tarjetas esperadas.

6. **Partidos con Mayor número de Córners Esperados**
    - **Descripción:** Este reporte proporciona detalles sobre los partidos con el mayor número de córners esperados, lo
      que puede indicar encuentros con un alto nivel de actividad en las áreas de juego.
    - **Datos del Informe:** Fecha del partido, Equipos involucrados, Promedio de córners esperados.

7. **Equipos con Mayor Promedio de Goles**
    - **Descripción:** Este reporte identifica los equipos con el promedio más alto de goles marcados por partido. Es
      útil para identificar equipos ofensivamente fuertes.
    - **Datos del Informe:** Nombre del equipo, Liga del equipo, Promedio de goles marcados por partido.

8. **Equipos con Mayor Promedio de Tarjetas Recibidas**
    - **Descripción:** Este reporte identifica los equipos con el promedio más alto de tarjetas amarillas y rojas
      recibidas por partido. Puede ser relevante para evaluar el comportamiento disciplinario de los equipos.
    - **Datos del Informe:** Nombre del equipo, Liga del equipo, Promedio de tarjetas amarillas recibidas, Promedio de
      tarjetas rojas recibidas.

9. **Equipos con Mejor Rendimiento en la temporada**
    - **Descripción:** Este informe identifica los equipos con el mejor rendimiento en la temporada, basado en su número
      de victorias y desempeño general.
    - **Datos del Informe:** Nombre del equipo, Liga del equipo, Número de victorias obtenidas.

10. **Equipos con Menor Promedio de Goles**
    - **Descripción:** Este reporte destaca los equipos con el promedio más bajo de goles marcados por partido, lo que
      puede identificar equipos más defensivos o con menor potencial de goles.
    - **Datos del Informe:** Nombre del equipo, Liga del equipo, Promedio de goles marcados por partido.
