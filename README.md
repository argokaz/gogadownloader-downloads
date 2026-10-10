# GogaDownloader

Descarga video o audio de **YouTube, Instagram, TikTok y X** desde una app nativa. Pega el enlace, elige video o audio y descarga. Las opciones avanzadas se despliegan cuando las necesitas.

[Visita la web oficial](https://gogadownloader.vercel.app/) para conocer la app y consultar la guía de instalación.

## Descargar 1.7.2

| Sistema | Descarga |
| --- | --- |
| **Mac con chip M1, M2, M3 o posterior** · macOS 13+ | [Descargar para Mac · Apple Silicon](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.2/GogaDownloader-1.7.2-Mac-Apple-Silicon.zip) |
| **Windows 11 · x64** | [Descargar instalador para Windows](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.2/GogaDownloader-1.7.2-Windows-Instalador.exe) |
| Windows · versión portable | [ZIP portable](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.2/GogaDownloader-1.7.2-Windows-Portable.zip) |

[Todos los archivos](https://github.com/argokaz/gogadownloader-downloads/releases/tag/v1.7.2) · [SHA-256](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.2/SHA256SUMS)

En Mac, descomprime y mueve GogaDownloader.app a Applications o a ~/Applications. En Windows, ejecuta el instalador por usuario. Para la actualización integrada de Windows se recomienda el instalador; la edición portable es una alternativa manual. No hay un paquete Mac Intel en esta release.

## Corrección de actualización en Mac

La versión **1.7.2** cierra el panel de Herramientas antes de instalar y reiniciar. Si una versión anterior muestra «El reinicio se canceló», **cierra la app y reemplázala manualmente una vez con este ZIP**. El arreglo debe estar instalado para que los reinicios futuros puedan usarlo. No se borran preferencias, motores mutables ni descargas.

Windows conserva el comportamiento de 1.7.1 y se recompila con la versión nueva para mantener su feed de actualizaciones completo.

## Qué puedes hacer

- Video recomendado: MP4 H.264/AAC hasta 1080p, sin recodificar.
- Modo rápido: MP4 hasta 720p, sin conversión.
- Audio M4A conservando AAC y conversiones explícitas a MP3, FLAC y Opus.
- Calidad original en MKV y conversión explícita a MP4 hasta 4K.
- Vista previa opcional, progreso, cancelación y acceso al archivo final.
- Reanudación de descargas parciales y diagnóstico secundario cuando falla un intento.
- Revisar actualizaciones de la app; los motores yt-dlp y FFmpeg/FFprobe se actualizan por separado.

La resolución y disponibilidad dependen de la fuente. La app no elude las restricciones del servicio.

## Reportar un problema

Al fallar una descarga, pulsa **Reportar problema…**. Revisa el diagnóstico y elige copiarlo, guardar TXT o abrir un borrador dirigido a **admin@arturogoga.com**. Tú decides si lo envías desde tu cliente de correo. El último reporte se recupera desde Herramientas.

No se adjuntan enlaces ni títulos de videos, carpetas, IP, cookies o credenciales. No se envía telemetría ni correo automáticamente.

## Paquetes y verificación

La corrección Mac pasó una regresión nativa con un panel SwiftUI real: primero se reprodujo el fallo original y después se verificó cierre, reemplazo, relanzamiento, firma, respaldo y conservación de datos en bundles temporales.

Windows 1.7.2 pasó 167 checks con motores directos y 183 con motores comprimidos, build WinUI y auditoría del instalador. El instalador, portable y paquete de actualización se analizaron con Defender el 10 de octubre de 2026 sin detecciones; [consulta el informe con hashes](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.2/GogaDownloader-Windows-1.7.2-Defender-Scan.json). Esta release Windows no recibió una nueva instalación ni prueba de interfaz en la Ally.

Los motores mantienen los bytes auditados de las versiones anteriores. Las fuentes, recetas y avisos correspondientes se adjuntan a la release. No necesitas descargar esos archivos para usar la app; los feeds y nupkg son para el actualizador.

Los paquetes no tienen certificados comerciales. Mac usa firma ad hoc y no está notarizada; Windows no tiene firma Authenticode. La web explica el primer inicio en Mac. Los checksums verifican integridad; no se presentan como firma de un publisher ni como certificación antivirus.

Este repositorio distribuye las apps y los componentes de terceros. El código de desarrollo se mantiene en un repositorio privado.
