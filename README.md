# Bobobo-bo Bo-bobo: Ougi 87.5 Bakuretsu Hanage Shinken — Traducción al español

[![Invítame a un café en Ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/johanderohan)

Ficha del proyecto, capturas y más traducciones al castellano en **[Parches en Castellano](https://parchesencastellano.com/traducciones/game-boy-advance/bobobo-ougi-87-5)**.

Traducción al **español de España** de *Bobobo-bo Bo-bobo: Ougi 87.5 Bakuretsu Hanage Shinken*
(ボボボーボ・ボーボボ 奥義87.5 爆烈鼻毛真拳, Game Boy Advance, Hudson Soft, 2002), el RPG del Puño del Pelo
Nasal que solo salió en Japón.

La traducción se ha hecho **directamente desde el japonés** del cartucho y se reparte como **parche**: no incluye
el juego. Necesitas tu propia copia de la versión japonesa para aplicarlo.

## Estado

Versión: **[v1.0](../../releases/tag/v1.0)** — primera versión publicada, **en revisión**.

| Parte | Estado |
|---|---|
| Guion de la historia y diálogos de los mapas | Traducido (todas las escenas: 7.574 textos en 1.759 guiones) |
| Técnicas y gritos de combate | Traducidos (481 secuencias de técnica, incluidos los gritos en letra grande) |
| Tragaperras de Palabras | Las 589 Palabras traducidas y coordinadas con las 155 técnicas que forman |
| Menús, objetos, tienda, posada, opciones, guardar/cargar, modo 2 jugadores | Traducidos |
| Rótulos dentro de imágenes | 32 rótulos funcionales traducidos (menú principal, barra de combate, estado, rangos, tragaperras…) |
| Teclado de nombre | Teclado latino con mayúsculas, minúsculas, Ñ, tildes, ¡ y ¿ |
| Créditos | Puestos traducidos y nombres romanizados |
| Caracteres españoles | **á é í ó ú ü ñ Á É Í Ó Ú Ü Ñ ¡ ¿ « »** |

Se mantienen tal cual el logotipo del título, el copyright y los rótulos que ya estaban en inglés («HAJIKE POINT»).
La terminología sigue el doblaje castellano de la serie (Bobobo, Beauty, Don Patch, Softon, Bola de Billar IV,
Cazadores de Pelo, Puño del Pelo Nasal) y, para el imperio, la edición española del manga (Imperio Calvorota).

### Cómo se ha hecho

- El juego dibuja cada carácter en una casilla fija de 12 píxeles pensada para japonés. Para que quepa el castellano
  se ha creado una fuente estrecha y cada casilla muestra **dos letras**; así caben 26 letras por línea en los
  cuadros de diálogo, con el mismo contraste (tinta blanca y contorno negro) que el original. Los gritos en letra
  grande usan la misma técnica a doble tamaño.
- Los guiones se reconstruyen y reubican en una ROM ampliada a 16 MiB; nada se recorta para que quepa.
- En el tragaperras de Palabras, la pantalla de resultado de la técnica se ha pasado de columnas verticales a filas
  horizontales para que se lea en castellano.
- Traducción, revisión y pruebas se han hecho con asistencia de IA, con una segunda lectura cotejada con el japonés
  de todos los textos. **No ha habido una revisión humana independiente.**

### Comprobaciones y limitaciones

Se ha jugado en emulador (mGBA) desde partida nueva: prólogo, Aldea Inafu, mapa del mundo y Base de la División G,
con combates, tragaperras, posada, tienda y guardado/carga comprobado tras reiniciar. La segunda mitad del juego
(Ciudad Demodé, Fantasilandia, Anillo de Gomina, Monte Narikatagi, Castillo del Rey Demonio Flor…) se ha revisado
lanzando sus escenas y combates de jefe con herramientas de prueba, no jugando de forma continua. También se han
visto el final y los créditos, el modo 2 jugadores (sin cable) y el teclado de nombre.

- **No se ha completado una partida de principio a fin** en condiciones normales, ni se ha probado en una consola real.
- Las escenas cuyo texto depende del progreso se han revisado con una partida recién empezada; puede haber variantes
  no vistas en pantalla.
- En la letra grande, las letras estrechas (como la «i») dejan algo de aire: «¡Miaaaau!!» se lee casi como «¡Mi aaaau!!».
- Algunos gritos que en japonés ocupan dos páginas siguen ocupando dos («¡Cuidado, / Bobobo!»).
- Las Palabras del tragaperras se muestran en el orden fijo del japonés, así que algunas técnicas se leen con un orden
  poco natural («Técnica dual / Pelo / Nasal / Ventosero / Puño»). La lista de Palabras conserva el orden original.
- Siguen en japonés los letreros pintados en los mapas y algún rótulo decorativo menor.

## Cómo aplicar el parche

1. Descarga `Bobobo.Ougi.87.5.ES.v1.0.xdelta` de la sección **[Releases](../../releases)**.
2. Consigue tu copia del juego en versión **japonesa**. El parche solo funciona con esa versión exacta.
3. **Comprueba que tu copia es la correcta** antes de nada:

   | | |
   |---|---|
   | Archivo | `Boboboubo Boubobo - Ougi 87.5 Bakuretsu Hanage Shinken (Japan).gba` |
   | Código de juego | `A8VJ` |
   | Tamaño | 8.388.608 bytes (8 MiB) |
   | MD5 | `ce085f9eb00a26cf9535172acc99921c` |
   | CRC32 | `58105f89` |

   ```bash
   md5sum "Boboboubo Boubobo - Ougi 87.5 Bakuretsu Hanage Shinken (Japan).gba"     # Linux
   md5 "Boboboubo Boubobo - Ougi 87.5 Bakuretsu Hanage Shinken (Japan).gba"        # macOS
   CertUtil -hashfile "Boboboubo Boubobo - Ougi 87.5 Bakuretsu Hanage Shinken (Japan).gba" MD5   # Windows
   ```

   Si no coincide, el parche fallará o dará un resultado corrupto.
4. Aplica el parche con una de estas herramientas:
   - **Windows**: [Delta Patcher](https://github.com/marco-calautti/DeltaPatcher/releases)
   - **Linux / macOS**: `xdelta3 -d -s "juego original.gba" Bobobo.Ougi.87.5.ES.v1.0.xdelta "juego traducido.gba"`
5. Comprueba que la ROM resultante mide **16.777.216 bytes (16 MiB)** y tiene MD5
   **`f90813210b2e140aad6112af31ca8e1b`**.
6. Carga la ROM resultante en tu emulador o flashcard preferidos. Usa el guardado interno del juego (Flash de 128 KiB);
   no mezcles estados instantáneos de otras versiones.

Aplica el parche siempre sobre la **ROM japonesa original**, no sobre una ROM ya traducida.

## Cambios

### v1.0

- Primera versión: historia, combates, técnicas, Palabras, menús, objetos, tienda, opciones, créditos y rótulos
  funcionales traducidos al castellano, con fuente española y teclado latino.

## Aviso

Este proyecto es una traducción hecha por afición, sin ánimo de lucro y sin relación alguna con Hudson Soft,
Konami, Shueisha ni Yoshio Sawai. Aquí no se distribuye el juego ni ninguna parte de él: solo un parche que modifica
una copia que ya tengas.

Si eres el titular de los derechos y quieres que retire esto, abre una incidencia y lo hago.
