# X-Men — Traducción al castellano

[![Invítame a un café](https://img.shields.io/badge/Ko--fi-Apoyar%20el%20proyecto-ff5e5b?logo=ko-fi&logoColor=white)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/mega-drive/x-men)**.

Traducción al castellano de España de **X-Men para Mega Drive / Genesis**, a partir de la edición USA en inglés. Se distribuye únicamente un parche: necesitas una copia propia del juego original.

## Estado

**v1.0.1 — En revisión.** Traducción y revisión asistidas por IA, sin revisión humana independiente ni partida completa.

Incluye:

- Los 122 bloques de diálogo, con sus variantes para los cuatro héroes y dos jugadores; 201 líneas castellanas. Se conserva la pista de desactivar y después reiniciar el ordenador.
- Prólogo, desenlace, pantalla de reinicio del sistema, viaje al asteroide M y créditos.
- Las cuatro fichas: Gambito, Rondador Nocturno, Lobezno y Cíclope; poderes, origen y datos físicos convertidos al sistema métrico.
- Menús y rótulos gráficos: PULSA START, DIFICULTAD, PRINCIPIANTE, HÉROE, SUPERHÉROE y ELIGE HÉROE; mensajes de derrota y fin de partida.
- Tildes, Ñ y signos ¡¿, conservando las paletas y el contraste del juego.

Se mantienen los logotipos, los avisos legales, los nombres de los autores originales y las expresiones francesas o alemanas de los personajes. La música y los efectos de sonido no se han modificado.

### Comprobaciones y límites

La construcción comprueba punteros, controles, dimensiones de mapas, límites de memoria, contenido de los textos, checksum y regiones que deben permanecer intactas. Las fichas conservan sus 385 baldosas originales y los menús se mantienen dentro del máximo original de 61 baldosas y 11 sprites. El parche se ha reaplicado al original con resultado idéntico byte a byte; dos construcciones independientes producen la misma ROM.

En Genesis Plus GX se han comprobado arranque frío, título, prólogo, dificultad y selección; las cuatro fichas completas; inicio jugable con mensajes de Gambito, Rondador y Cíclope; movimiento, salto y pausa/salida. El desenlace, los créditos y la pantalla de reinicio se han ensayado mediante acceso dirigido en el emulador. La candidata final incluye la corrección de la cabecera de Rondador, que invadía la barra del HUD.

No se ha jugado de principio a fin ni probado en consola física. Las pruebas dirigidas de escenas posteriores eluden sus condiciones de acceso y no demuestran que toda la aventura se haya completado. No se ha revisado el modo de dos jugadores en una partida completa. El juego no incorpora guardado de partida; los estados del emulador son una función aparte. Empieza una partida nueva y crea estados nuevos con esta versión.

## Cómo aplicar el parche

1. Descarga **[X-Men-es-ES-v1.0.1.xdelta](https://github.com/johanderohan/x-men-traduccion-es/releases/download/v1.0.1/X-Men-es-ES-v1.0.1.xdelta)** de la sección [Releases](https://github.com/johanderohan/x-men-traduccion-es/releases).
2. Comprueba que tu copia es la ROM USA original, sin cabecera de copiador ni otros parches:

| Archivo | Tamaño | MD5 |
|---|---:|---|
| X-Men (USA).md | 1.048.576 bytes (1 MiB) | `63274bdd105d2abf265aa2d2934635c5` |
| Resultado castellano v1.0.1 | 2.097.152 bytes (2 MiB) | `0f2ecc71773e69409eb6e96e5970b09f` |

3. Usa Delta Patcher o ejecuta:

```sh
xdelta3 -d -s "X-Men (USA).md" X-Men-es-ES-v1.0.1.xdelta "X-Men (es-ES).md"
```

4. Comprueba el MD5 del resultado y ábrelo en tu emulador. Cada versión se aplica sobre el original limpio, nunca sobre una ROM ya traducida.

La extensión `.md` del archivo del juego corresponde a una ROM de Mega Drive. La ampliación a 2 MiB aloja recursos de traducción en el cartucho; no amplía los búferes de RAM ni la VRAM de la consola.

### Huellas SHA-256

- Original: `49f601abfa61f23f70420a2cc0c4cc90273540b4d199fb61d516f6344e9067ef`
- Resultado v1.0.1: `f37f4b16ed62ef58de17a08cde76fef1c93f679e667e255d7c53702c15aec7d7`
- Parche v1.0.1: `bee1de94b6a4a03a83a7bdedd7dd41c1f0bd58659614980a1a1ed62698d48b26`

## Cambios

### v1.0.1 · 27 de octubre de 2026

Corrige los dos puntos, que aparecían como guiones en siete frases de diálogo, desenlace y cartelas. Se reutiliza un glifo sin ampliar la VRAM. Comprobado el signo en el juego y que el HUD se restaura sin cambios al cerrar el diálogo. El codificador y la auditoría rechazan ahora caracteres sin glifo propio.

### v1.0 · 27 de octubre de 2026

Primera publicación: historia, diálogos, fichas, menús y créditos en castellano. Se recupera en dos cuadros el sentido de dos frases que estaban almacenadas sin una referencia accesible en la ROM original.

## Créditos y aviso legal

Traducción, adaptación de fuentes, herramientas y revisión: proyecto de johanderohan con asistencia de IA. Pruebas en Genesis Plus GX mediante libretro, en Linux. El arte de las letras se deriva de los glifos del propio juego.

Proyecto de aficionados sin relación con Marvel, SEGA ni Western Technologies. X-Men y el juego pertenecen a sus respectivos titulares. Este repositorio no incluye ROM, BIOS, guion extraído ni herramientas con contenido del juego: solo información del proyecto y el parche en las descargas. Si eres titular de derechos y quieres solicitar una retirada, abre una incidencia.
