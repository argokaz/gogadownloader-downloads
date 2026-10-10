# GogaDownloader

Descarga video o audio de **YouTube, Instagram, TikTok y X** desde una app nativa.
Pega el enlace, elige video o audio y descarga. Las opciones avanzadas se despliegan
cuando las necesitas.

[Visita el sitio oficial](https://gogadownloader.vercel.app/) para conocer la app y elegir tu descarga.

## Descargar 1.7.0

| Sistema | Descarga |
| --- | --- |
| **Mac · Apple Silicon** · macOS 13 o posterior | [ZIP para Mac](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.0/GogaDownloader-1.7.0-macOS-arm64.zip) |
| **Windows 11 · x64** | [Instalador para Windows](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.0/GogaDownloader-win-Setup.exe) |
| Windows · versión portable | [ZIP portable](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.0/GogaDownloader-win-Portable.zip) |

[Todos los archivos de la release](https://github.com/argokaz/gogadownloader-downloads/releases/tag/v1.7.0)
· [Checksums SHA-256](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.0/SHA256SUMS)

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

Si vienes de Mac 1.3 o Windows 1.6.0, instala 1.7.0 una vez desde esta página
para activar el canal público. Esas versiones anteriores todavía no conocen
el nuevo canal; no recibirán esta primera actualización automáticamente.

## Verificación y componentes

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
