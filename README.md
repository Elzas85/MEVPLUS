# MEV SCBA — Bajar expediente completo (fiel)

Userscript para **Tampermonkey** que descarga un expediente completo de la
[Mesa de Entradas Virtual (MEV) de la SCBA](https://mev.scba.gov.ar/) en un
**único PDF, en orden cronológico**, tal como la MEV lo presenta.

* Cada actuación se captura con la **presentación original** de la MEV (su
encabezado, tipografía y diagramación), no se recompone el texto.
* Los **adjuntos** se incorporan tal cual vienen (conservan firma, sellos y
formato) y quedan justo detrás del proveído o escrito al que pertenecen.
* Cada página lleva una **capa de texto invisible**, así el PDF sigue siendo
buscable con Ctrl+F aunque las actuaciones sean imágenes.
* Convive con la **validación anti-bot** de la MEV: espera, la resuelve y
sigue desde donde estaba, sin perder lo descargado.

## Cómo se usa

1. Instalá [Tampermonkey](https://www.tampermonkey.net/) en tu navegador.
2. Compatible con Sistemas Operativos que tengan Navegador que acepte Tampermonkey, como Windows, Linux y Macos
3. Instalá este script (ver más abajo).
4. Entrá a la MEV y abrí el **listado de actuaciones** de una causa.
5. Abajo a la derecha aparece el panel **Bajar expediente**. Elegí qué bajar:

   * **Todo:** viene todo tildado; tocá *Bajar seleccionadas*.
   * **Por fechas:** poné un rango en *Fechas* y *Marcar*.
   * **A mano:** tildá o destildá actuaciones. El buscador filtra por fecha o
texto; *Todas / Ninguna / Invertir* actúan sobre lo que el filtro deja a
la vista.
5. El botón baja exactamente lo seleccionado, en orden cronológico.

Si la MEV está validando el acceso, dejá la pestaña quieta unos segundos o usá
**recargar página**; el script retoma solo.

## Instalación

1. Tené [Tampermonkey](https://www.tampermonkey.net/) instalado.
2. Hacé clic en el enlace de instalación:
[**Instalar mev-bajar-expediente.user.js**](https://raw.githubusercontent.com/Elzas85/BAJAR-EXPEDIENTE-DE-LA-MEV/main/mev-bajar-expediente.user.js)
3. Tampermonkey detecta el userscript y abre la pantalla de instalación. Tocá *Instalar*.

Tampermonkey chequea ese mismo enlace para **actualizarse solo** cuando publiques
una versión nueva.

Las librerías `pdf-lib` y `html2canvas` las descarga Tampermonkey solo desde el
CDN (`@require`); no hay que instalar nada más.

## Autor

Creado por **Ignacio Kinbaum** con Claude.
Contacto: estudiojuridicokinbaum@gmail.com

## Licencia

Copyleft — **GNU General Public License v3.0 o posterior** ([GPL-3.0-or-later](LICENSE)).

Software libre: se permite y se alienta su uso, copia, modificación y
distribución de forma gratuita, siempre que las obras derivadas conserven esta
misma licencia. Sin garantía.

