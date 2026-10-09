# GogaDownloader

Descarga video o audio de **YouTube, Instagram, TikTok y X** desde una app nativa.
Pega el enlace, elige video o audio y descarga. Las opciones avanzadas se despliegan
cuando las necesitas.

[Visita el sitio oficial](https://gogadownloader.vercel.app/) para conocer la app y elegir tu descarga.

## Descargar 1.6.1

| Sistema | Descarga |
| --- | --- |
| **Mac · Apple Silicon** · macOS 13 o posterior | [ZIP para Mac](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.6.1/GogaDownloader-1.6.1-macOS-arm64.zip) |
| **Windows 11 · x64** | [Instalador para Windows](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.6.1/GogaDownloader-win-Setup.exe) |
| Windows · versión portable | [ZIP portable](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.6.1/GogaDownloader-win-Portable.zip) |

[Todos los archivos de la release](https://github.com/argokaz/gogadownloader-downloads/releases/tag/v1.6.1)
· [Checksums SHA-256](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.6.1/SHA256SUMS)

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
- Actualización de la app y de los motores por separado; las descargas activas
  bloquean el reinicio para instalar.

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

El engranaje permite buscar actualizaciones de la aplicación y de los motores.
Mac consulta la release estable y verifica el ZIP antes de **Instalar y reiniciar**;
conserva una copia anterior. Windows usa Velopack con el feed de este repositorio.
No se reemplazan motores durante descargas o conversiones.

Si vienes de Mac 1.3 o Windows 1.6.0, instala 1.6.1 una vez desde esta página
para activar el canal público. Esas versiones anteriores todavía no conocen
el nuevo canal; no recibirán esta primera actualización automáticamente.

## Verificación y componentes

Mac 1.6.1 se comprobó en un Mac Apple Silicon: descargas públicas de las cuatro
plataformas, MP4 compatible, MKV original, extracción AAC/M4A, cancelación y
actualización real entre bundles de prueba. La interfaz se revisó en claro y
oscuro, con opciones plegadas y desplegadas.

Windows conserva la interfaz y los servicios validados en la ROG Ally con
1.5.1/1.6.0. El paquete público 1.6.1 se compiló y comprobó en Windows nativo en
GitHub Actions, incluidos los motores propios, Core y contenido del instalador.
No se presenta como una nueva prueba de UI/AMF en la Ally ni como instalación
verificada en una VM limpia.

El instalador, el portable y el paquete de actualización de Windows 1.6.1
se analizaron con Microsoft Defender el 9 de octubre de 2026, con firmas actuales
y sin detecciones. El [informe con los hashes exactos](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.6.1/GogaDownloader-Windows-1.6.1-Defender-Scan.json)
registra esos archivos y esa fecha; no es una certificación ni una garantía
absoluta de ausencia de malware. No se declara un análisis antivirus de Mac.

Los paquetes incluyen avisos de terceros. Las fuentes correspondientes de
FFmpeg/FFprobe, sus bibliotecas y los componentes identificados del standalone
yt-dlp se adjuntan a la release, con receta, versiones y hashes. Deno y 7-Zip
conservan sus avisos y fuentes originales. Las fuentes de terceros no requieren
descarga para usar la aplicación.

Este repositorio distribuye las apps y componentes de terceros. El código de
desarrollo de GogaDownloader se mantiene en un repositorio privado.
