# <a name="titulo1"></a>**Descripción del caso**

<p><strong>Usuario (FUERTE):</strong></p>
<ul>
  <li class="red-gt">ID del usuario</li>
  <li class="red-gt">Nombre</li>
  <li class="red-gt">Fecha de registro</li>
  <li class="red-gt">Liga de preferencia</li>
</ul>

## Aplicación

En el mundo del deporte, las apuestas son una actividad común y emocionante. Sin embargo, hacer pronósticos precisos
puede ser un desafío debido a la cantidad de variables involucradas. Para abordar este problema, se propone el
desarrollo de un “Pronosticador Deportivo”. Este sistema no es simplemente una herramienta de apuestas, sino una
plataforma de análisis deportivo que utiliza una base de datos relacional para proporcionar a los usuarios información
detallada y pronósticos precisos para apuestas deportivas de fútbol en partidos de ligas específicas.

La aplicación utilizará un gran conjunto de estadísticas, tanto generales como detalladas, que incluyen victorias,
derrotas, empates, puntos totales, goles, córners y tarjetas obtenidas por los equipos hasta un punto determinado de la
temporada. Con estos datos, la aplicación buscará predecir resultados futuros en términos de tarjetas, córners y goles
en los próximos partidos.

La entidad principal en este proyecto es “`Partido`”. En ella se registran los datos relevantes de cada encuentro,
incluyendo el equipo local y visitant, el árbitro del partido y las estadísticas esperadas. Esta entidad será la piedra
angular para el análisis y las predicciones que la aplicación proporcionará a sus usuarios. Además, la aplicación
también considerará otras entidades importantes como “`Usuario`”, “`Equipo`”, “`Liga`”, “`Árbitro`” y “`Estadísticas`”,
cada una con su propio conjunto de atributos que contribuyen a la variedad de los datos disponibles para el análisis.

En resumen, el “Pronosticador Deportivo” es una herramienta integral diseñada para mejorar la experiencia de las
apuestas deportivas, proporcionando a los usuarios análisis detallados y pronósticos precisos.

## Objetivos

El objetivo de la aplicación de "Pronosticador Deportivo" es proporcionar a los usuarios una plataforma integral para el
análisis y pronóstico de resultados en partidos de fútbol de ligas específicas. Para ello se debe cumplir:

1. **Análisis detallado:** La aplicación recopilará y analizará estadísticas relacionadas con los equipos, árbitros y
   otros factores relevantes para los partidos de fútbol. Esto incluirá datos como victorias, derrotas, empates, puntos
   totales, goles, córners y tarjetas obtenidas por los equipos hasta un punto específico de la temporada.

2. **Predicción de resultados:** Utilizando los datos recopilados, la aplicación buscará predecir resultados futuros en
   términos de tarjetas, córners y goles en los próximos partidos.

3. **Mejora de la experiencia de apuestas deportivas:** El objetivo final es mejorar la experiencia de las apuestas
   deportivas para los usuarios al proporcionarles información detallada y pronósticos confiables. Esto permitirá a los
   usuarios tomar decisiones más informadas al realizar sus apuestas, lo que potencialmente aumentará sus posibilidades
   de éxito.

## Entidades y relaciones

### Entidades

**Usuario (FUERTE):**

```bash
> ID del usuario
> Nombre
> Fecha de registro
> Liga de preferencia
```

**Equipo (FUERTE):**

```bash
> ID del equipo
> ID de la liga
> Nombre del equipo
> Estadio
```

**Liga (FUERTE):**

```bash
> ID de la liga
> Nombre de la liga
> País
> Número de equipos
```

**Árbitro (FUERTE):**

```bash
> ID del árbitro
> ID de la liga
> Nombre del árbitro
> Promedio de tarjetas amarillas
> Promedio de tarjetas rojas
```

**Partido (DÉBIL):**

```console
> ID del partido
> Fecha del partido
> ID equipo local
> ID equipo visitante
> ID del árbitro
> Promedio de goles esperados
> Promedio de córners esperados
> Promedio de tarjetas esperadas
```

**Estadísticas (DÉBIL):**

```bash
> ID del equipo
> Número de victorias
> Número de derrotas
> Número de empates
> Puntos totales en la temporada
> Promedio de goles
> Promedio de córners a favor
> Promedio de córners en contra
> Promedio de tarjetas a favor
> Promedio de tarjetas en contra
```

### Relaciones

1. **Usuario - Liga**
    - **Descripción:** Un usuario tiene una liga de preferencia. Por lo tanto, existe una relación de uno a uno entre el
      Usuario y la Liga.
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
    - **Datos del Informe:** Nombre del equipo, Promedio de tarjetas amarillas recibidas, Promedio de tarjetas amarillas
      concedidas, Promedio de tarjetas rojas recibidas, Promedio de tarjetas rojas concedidas.

2. **Equipos con Más Victorias**
    - **Descripción:** Este reporte identifica los equipos con el mayor número de victorias, proporcionando una visión
      clara de los equipos más exitosos en términos de resultados.
    - **Datos del Informe:** Nombre del equipo, Número de victorias.

3. **Partidos con Más Goles Esperados**
    - **Descripción:** Este reporte destaca los partidos con la mayor expectativa de goles, basándose en el promedio de
      goles esperados de los equipos participantes. Ayuda a identificar los encuentros más emocionantes en términos de
      potencial de puntuación.
    - **Datos del Informe:** Fecha del partido, Equipos involucrados, Promedio de goles esperados.

4. **Árbitros con Más Tarjetas**
    - **Descripción:** Este reporte identifica a los árbitros que han mostrado más tarjetas amarillas y rojas. Es útil
      para evaluar el estilo de arbitraje y su impacto en el desarrollo del juego.
    - **Datos del Informe:** Nombre del árbitro, Promedio de tarjetas amarillas mostradas, Promedio de tarjetas rojas
      mostradas.

5. **Partidos con Menos Tarjetas Esperadas**
    - **Descripción:** Este reporte destaca los partidos con la menor expectativa de tarjetas amarillas y rojas,
      basándose en el promedio de tarjetas esperadas de los equipos participantes. Puede ser relevante para aquellos
      interesados en partidos con menor tensión disciplinaria.
    - **Datos del Informe:** Fecha del partido, Equipos involucrados, Promedio de tarjetas esperadas.

6. **Número de Córners de un Partido Específico**
    - **Descripción:** Este reporte permite obtener información sobre la cantidad de córners generados durante un
      partido específico. Es útil para evaluar la presión ejercida por los equipos en el área rival y su capacidad para
      crear oportunidades de gol a partir de córners.
    - **Datos del Informe:** Fecha del partido, Equipos involucrados, Número de córners.

7. **Equipos con Mayor Promedio de Goles**
    - **Descripción:** Este reporte identifica los equipos con el promedio más alto de goles marcados por partido. Es
      útil para identificar equipos ofensivamente fuertes.
    - **Datos del Informe:** Nombre del equipo, Promedio de goles marcados por partido.

8. **Partidos con Menor Promedio de Goles**
    - **Descripción:** Este reporte destaca los partidos con el promedio más bajo de goles marcados por partido, lo que
      puede indicar encuentros más defensivos o con menor potencial de puntuación.
    - **Datos del Informe:** Fecha del partido, Equipos involucrados, Promedio de goles marcados por partido.

9. **Equipos con Mayor Promedio de Tarjetas Recibidas**
    - **Descripción:** Este reporte identifica los equipos con el promedio más alto de tarjetas amarillas y rojas
      recibidas por partido. Puede ser relevante para evaluar el comportamiento disciplinario de los equipos.
    - **Datos del Informe:** Nombre del equipo, Promedio de tarjetas amarillas recibidas, Promedio de tarjetas rojas
      recibidas.

10. **Partidos con Mayor Diferencia de Goles**
    - **Descripción:** Este reporte identifica los partidos con la mayor diferencia de goles entre los equipos
      participantes, lo que puede indicar encuentros especialmente desequilibrados o dominantes por parte de un equipo.
    - **Datos del Informe:** Equipos involucrados, Diferencia de goles.

> [!IMPORTANT]
> La concepción de nuestra aplicación, el “Pronosticador Deportivo”, se sitúa en un equilibrio entre la originalidad y
> la adaptación. Nos inspiramos en plataformas consolidadas como "[OneFootball](https://onefootball.com/es/inicio)" y
> "[FlashScore](https://www.flashscore.co/)" para la recopilación de estadísticas de equipos. Sin embargo, sentimos que
> eso no era suficiente. Por lo que, decidimos incorporar un componente de predicción para los próximos partidos,
> basándonos en fórmulas de cálculo de estadísticas disponibles en recursos públicos, como los videos
> de "[El Capi](https://www.youtube.com/@elcapi_sports)" en YouTube. Por ese motivo no consideramos la idea cien por
> ciento original o adaptada, sino una combinación innovadora de ambos.
