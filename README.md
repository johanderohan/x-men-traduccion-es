# X-Men — Traducción al castellano

[![Invítame a un café](https://img.shields.io/badge/Ko--fi-Apoyar%20el%20proyecto-ff5e5b?logo=ko-fi&logoColor=white)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/mega-drive/x-men)**.

Traducción al castellano de España de **X-Men para Mega Drive / Genesis**, a partir de la edición USA en inglés. Se distribuye únicamente un parche: necesitas una copia propia del juego original.

## Estado

**v1.1 — En revisión.** Traducción y revisión asistidas por IA, sin revisión humana independiente ni partida completa.

Incluye:

- Los 122 bloques de diálogo, con sus variantes para los cuatro héroes y dos jugadores; 201 líneas castellanas. Se conserva la pista de desactivar y después reiniciar el ordenador.
- Prólogo, desenlace, pantalla de reinicio del sistema, viaje al asteroide M y créditos.
- Las cuatro fichas: Gambito, Rondador Nocturno, Lobezno y Cíclope; poderes, origen y datos físicos convertidos al sistema métrico.
- Menús y rótulos gráficos: PULSA START (título, selección y demostraciones), DIFICULTAD, PRINCIPIANTE, HÉROE, SUPERHÉROE y ELIGE HÉROE; la frase de Magneto al empezar; mensajes de derrota y fin de partida.
- Tildes, Ñ y signos ¡¿, conservando las paletas y el contraste del juego.

Se mantienen los logotipos, los avisos legales, los nombres de los autores originales y las expresiones francesas o alemanas de los personajes. La música y los efectos de sonido no se han modificado.

### Comprobaciones y límites

La construcción comprueba punteros, controles, dimensiones de mapas, límites de memoria, contenido de los textos, checksum y regiones que deben permanecer intactas. Las fichas conservan sus 385 baldosas originales y los menús se mantienen dentro del máximo original de 61 baldosas y 11 sprites. El parche se ha reaplicado al original con resultado idéntico byte a byte; dos construcciones independientes producen la misma ROM.

En Genesis Plus GX se han comprobado arranque frío, título, prólogo, dificultad y selección; las cuatro fichas completas; inicio jugable con mensajes de Gambito, Rondador y Cíclope; movimiento, salto y pausa/salida. El desenlace, los créditos y la pantalla de reinicio se han ensayado mediante acceso dirigido en el emulador. La v1.1 se ha comprobado además desde arranque frío en la frase de Magneto, la demostración con PULSA START, las cuatro fichas con su desplazamiento, los signos ¡¿ del primer diálogo y la pantalla de reinicio del sistema.

No se ha jugado de principio a fin ni probado en consola física. Las pruebas dirigidas de escenas posteriores eluden sus condiciones de acceso y no demuestran que toda la aventura se haya completado. No se ha revisado el modo de dos jugadores en una partida completa. El juego no incorpora guardado de partida; los estados del emulador son una función aparte. Empieza una partida nueva y crea estados nuevos con esta versión.

## Cómo aplicar el parche

1. Descarga **[X-Men-es-ES-v1.1.xdelta](https://github.com/johanderohan/x-men-traduccion-es/releases/download/v1.1/X-Men-es-ES-v1.1.xdelta)** de la sección [Releases](https://github.com/johanderohan/x-men-traduccion-es/releases).
2. Comprueba que tu copia es la ROM USA original, sin cabecera de copiador ni otros parches:

| Archivo | Tamaño | MD5 |
|---|---:|---|
| X-Men (USA).md | 1.048.576 bytes (1 MiB) | `63274bdd105d2abf265aa2d2934635c5` |
| Resultado castellano v1.1 | 2.097.152 bytes (2 MiB) | `3a89b018bca3247b1ffdf6b60bf395bb` |

3. Usa Delta Patcher o ejecuta:

```sh
xdelta3 -d -s "X-Men (USA).md" X-Men-es-ES-v1.1.xdelta "X-Men (es-ES).md"
```

4. Comprueba el MD5 del resultado y ábrelo en tu emulador. Cada versión se aplica sobre el original limpio, nunca sobre una ROM ya traducida.

La extensión `.md` del archivo del juego corresponde a una ROM de Mega Drive. La ampliación a 2 MiB aloja recursos de traducción en el cartucho; no amplía los búferes de RAM ni la VRAM de la consola.

### Huellas SHA-256

- Original: `49f601abfa61f23f70420a2cc0c4cc90273540b4d199fb61d516f6344e9067ef`
- Resultado v1.1: `9c6148a670bfe9b7b7729d9efe190137dfb478ceafd944ee56472d48e186e937`
- Parche v1.1: `36addb4f6d3ab97d28e3011b5729e1fa9bdfd586ba4ea66732220109fd6ff72a`

## Fase del ordenador: hay que reiniciar la consola

En el escenario del ordenador (Sala de Peligro), tras desactivar el virus el juego pide reiniciar el ordenador. Hay que pulsar **Reset** de la consola (en el emulador, la opción de reinicio suave) sin volver a cargar la ROM; entonces aparece la pantalla verde de reinicio del sistema y continúa la historia. Es una mecánica del juego original, no un cuelgue de la traducción.

## Cambios

### v1.1 · 30 de octubre de 2026

Traducidos la frase inicial de Magneto y el rótulo PULSA START de las demostraciones, que seguían en inglés. En las fichas, las cabeceras ya no dejan ver el texto que se desplaza detrás y las letras se bajan para que las tildes no deformen las mayúsculas. Los signos ¡ y ¿ se alinean con el resto de la línea. El cursor de la pantalla de reinicio vuelve a ser un bloque en lugar de una Á. Recoge los comentarios de un usuario; aplica el parche sobre el original limpio.

### v1.0.1 · 27 de octubre de 2026

Corrige los dos puntos, que aparecían como guiones en siete frases de diálogo, desenlace y cartelas. Se reutiliza un glifo sin ampliar la VRAM. Comprobado el signo en el juego y que el HUD se restaura sin cambios al cerrar el diálogo. El codificador y la auditoría rechazan ahora caracteres sin glifo propio.

### v1.0 · 27 de octubre de 2026

Primera publicación: historia, diálogos, fichas, menús y créditos en castellano. Se recupera en dos cuadros el sentido de dos frases que estaban almacenadas sin una referencia accesible en la ROM original.

## Créditos y aviso legal

Traducción, adaptación de fuentes, herramientas y revisión: proyecto de johanderohan con asistencia de IA. Pruebas en Genesis Plus GX mediante libretro, en Linux. El arte de las letras se deriva de los glifos del propio juego.

Proyecto de aficionados sin relación con Marvel, SEGA ni Western Technologies. X-Men y el juego pertenecen a sus respectivos titulares. Este repositorio no incluye ROM, BIOS, guion extraído ni herramientas con contenido del juego: solo información del proyecto y el parche en las descargas. Si eres titular de derechos y quieres solicitar una retirada, abre una incidencia.
