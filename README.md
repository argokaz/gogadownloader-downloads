# GogaDownloader

Descarga video o audio de **YouTube, Instagram, TikTok y X** desde una app nativa.
Pega el enlace, elige video o audio y descarga. Las opciones avanzadas se despliegan
cuando las necesitas.

[Visita el sitio oficial](https://gogadownloader.vercel.app/) para conocer la app y elegir tu descarga.

## Descargar 1.7.1

| Sistema | Descarga |
| --- | --- |
| **Mac con chip M1, M2, M3 o posterior** · macOS 13+ | [Descargar para Mac · Apple Silicon](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.1/GogaDownloader-1.7.1-Mac-Apple-Silicon.zip) |
| **Windows 11 · x64** | [Descargar instalador para Windows](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.1/GogaDownloader-1.7.1-Windows-Instalador.exe) |
| Windows · versión portable | [ZIP portable](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.1/GogaDownloader-1.7.1-Windows-Portable.zip) |

[Todos los archivos de la release](https://github.com/argokaz/gogadownloader-downloads/releases/tag/v1.7.1)
· [Checksums SHA-256](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.1/SHA256SUMS)

En Mac, descomprime y mueve GogaDownloader.app a Applications o a ~/Applications.
En Windows, ejecuta el instalador por usuario. La edición portable se extrae en
una carpeta; para actualización integrada se recomienda el instalador.

Los paquetes no tienen certificados comerciales. La versión Mac lleva firma ad
hoc y no está notarizada; Windows no tiene firma Authenticode. El sistema puede
mostrar una advertencia o bloquear el primer inicio. Compara el SHA-256 con
el publicado antes de abrir el paquete.

## Qué puedes hacer

- Video recomendado: MP4 H.264/AAC hasta 1080p, sin recodificar.
- Modo rápido: MP4 hasta 720p, sin conversión.
- Audio M4A conservando AAC, o conversión explícita a MP3, FLAC y Opus.
- Calidad original en MKV y conversión explícita a MP4 hasta 4K.
- Vista previa opcional, progreso, cancelación y acceso al archivo final.
- Pegar y descargar con la calidad y carpeta visibles, sin vista previa obligatoria.
- Inicio sin comprobaciones de motores en el hilo de interfaz; Windows comprueba
  AMF al pedir una conversión 4K explícita.
- Recuperación de parciales con el mismo enlace, calidad y destino, si la fuente
  permite continuar. Video, audio, unión y verificación se muestran por etapas.
- Actualización de la app y de los motores por separado; las descargas activas
  tienen prioridad sobre las transferencias de actualización y bloquean el reinicio.

La resolución depende de la fuente. En Mac, los videos verticales se limitan por
su lado corto; Windows comprueba la altura. Mac también puede separar AAC de un
video social sin recodificar. Si la fuente no ofrece un formato compatible, la
app lo indica y permite elegir otro.

Se descargan videos individuales. YouTube con playlist descarga solo el video
actual; en publicaciones múltiples se usa el primer elemento del extractor y
debe contener video. Perfiles, feeds y carruseles completos no están incluidos.
La disponibilidad, el inicio de sesión, la región y los límites de cada plataforma
pueden impedir la descarga. No se importan cookies del navegador automáticamente.

## Actualizaciones

En Herramientas, pulsa **Revisar actualizaciones**. Mac también ofrece esa acción
en el menú **GogaDownloader**. Busca las nuevas versiones publicadas en GitHub.
Mac consulta la release estable y verifica el ZIP antes de **Instalar y reiniciar**;
conserva una copia anterior. Windows usa Velopack con el feed de este repositorio.
Tú eliges cuándo instalar y reiniciar. No se reemplazan motores durante descargas
o conversiones. Para las actualizaciones integradas de la aplicación se recomienda
el instalador; la actualización entre versiones del ZIP portable no se ha verificado.

Si vienes de Mac 1.3 o Windows 1.6.0, instala 1.7.1 una vez desde esta página
para activar el canal público. Esas versiones anteriores todavía no conocen
el nuevo canal; no recibirán esta primera actualización automáticamente.

## Reportar un problema

Al fallar una descarga, pulsa **Reportar problema…**. Revisa el diagnóstico y
elige copiar, guardar TXT o abrir un borrador dirigido a **admin@arturogoga.com**.
Tú decides si lo envías desde tu cliente de correo. Si usas webmail, puedes
copiarlo o adjuntar el TXT. El último reporte se recupera desde Herramientas.

El reporte conserva la versión, plataforma, selección y fase del intento fallido,
junto a señales técnicas reconocidas. No adjunta enlaces ni títulos de videos,
rutas, IP, cookies o credenciales. No envía telemetría ni correos automáticamente.

## Verificación y componentes

La versión 1.7.1 pasó ocho suites de comprobaciones Mac, compilación arm64 y
revisión del diálogo de reporte en claro y oscuro. Windows pasó 167 checks con
motores directos y 183 con motores comprimidos, compilación WinUI autocontenida,
auditoría del instalador y comprobación de los alias de descarga. Los motores y
sus fuentes permanecen idénticos a los de 1.7.0.

El instalador, el portable y el paquete de actualización de Windows 1.7.1
se analizaron con Microsoft Defender el **10 de octubre de 2026**, sin detecciones.
El [informe con sus hashes](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.1/GogaDownloader-Windows-1.7.1-Defender-Scan.json)
registra archivos, firmas y fecha; no es una certificación. No se declara un
análisis antivirus de Mac ni entrega o recepción de correo.

En la ROG Ally se comprobó el visor de reportes completo en claro y oscuro,
el desplazamiento hasta la última línea, la copia de 23 líneas y la recuperación
íntegra tras reiniciar. Se usó una variante con datos y mutex de QA separados;
los paquetes públicos provienen de la CI nativa final. El selector TXT se abrió,
pero la automatización no permitió completar esa ventana; el mismo API de
escritura Windows sí conservó íntegro el contenido UTF-8 en una prueba nativa.
No se presenta esto como instalación del Setup público ni como prueba del perfil
habitual. La entrega de correo permanece bajo control del usuario.

### Evidencia de la versión anterior


Mac 1.7.0 pasó las comprobaciones de modelos, motores, procesos, validación de
medios, recuperación y actualización entre bundles de prueba. Se completó una
descarga real de YouTube a 1080p tras recuperar el parcial de un intento fallido.
Las pruebas locales de reanudación comprobaron HTTP Range y coincidencia exacta
de bytes al renovar el enlace CDN y cambiar el título. Las cuatro plataformas,
MKV y AAC/M4A se comprobaron en la versión 1.6.1; no se presenta esa evidencia
como una nueva descarga remota de las cuatro fuentes en 1.7.0.

Windows 1.7.0 pasó CI en Windows nativo: 146 comprobaciones con motores directos
y 162 con motores comprimidos, WinUI y auditoría del instalador. En la ROG Ally
pasaron Core, cancelación y reanudación reales, AMF y la alternativa CPU.
La interfaz observada era un build previo con los mismos archivos de UI.
La actualización de una app compilada localmente con el mismo código pasó
entre dos versiones de QA instaladas, con datos separados:
esperó a FFmpeg, bloqueó el reinicio durante el trabajo, conservó la actualización
ante un fallo del feed y relanzó la nueva versión. El perfil habitual quedó idéntico.
Esa prueba usó paquetes de QA; no instaló el Setup público exacto ni comprobó
el salto instalado habitual 1.6.0 → 1.7.0 o un trabajo desde la UI final.
Las lecturas puntuales de arranque no son un benchmark. No hay verificación
en una VM Windows limpia ni garantía de descarga de un contenido concreto.

El instalador, el portable y el paquete de actualización de Windows 1.7.0
se analizaron con Microsoft Defender el 9 de octubre de 2026 en Lima, sin detecciones. El [informe con los hashes exactos](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.0/GogaDownloader-Windows-1.7.0-Defender-Scan.json)
registra esos archivos y esa fecha; no es una certificación ni una garantía
absoluta de ausencia de malware. No se declara un análisis antivirus de Mac.

Los paquetes incluyen avisos de terceros. Las fuentes correspondientes de
FFmpeg/FFprobe, sus bibliotecas y los componentes identificados del standalone
yt-dlp se adjuntan a la release, con receta, versiones y hashes. Deno y 7-Zip
conservan sus avisos y fuentes originales. Las fuentes de terceros no requieren
descarga para usar la aplicación.

Este repositorio distribuye las apps y componentes de terceros. El código de
desarrollo de GogaDownloader se mantiene en un repositorio privado.
