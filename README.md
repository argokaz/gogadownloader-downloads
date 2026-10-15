# GogaDownloader

Descarga video o audio de **YouTube, Instagram, TikTok y X** desde una app nativa. Pega el enlace, elige video o audio y descarga. Las opciones avanzadas se despliegan cuando las necesitas.

[Visita la web oficial](https://gogadownloader.vercel.app/) para conocer la app y consultar la guía de instalación.

## Descargar 1.7.3

| Sistema | Descarga |
| --- | --- |
| **Mac con chip M1, M2, M3 o posterior** · macOS 13+ | [Descargar para Mac · Apple Silicon](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.3/GogaDownloader-1.7.3-Mac-Apple-Silicon.zip) |
| **Windows 11 · x64** | [Descargar instalador para Windows](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.3/GogaDownloader-1.7.3-Windows-Instalador.exe) |
| Windows · versión portable | [ZIP portable](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.3/GogaDownloader-1.7.3-Windows-Portable.zip) |

[Todos los archivos](https://github.com/argokaz/gogadownloader-downloads/releases/tag/v1.7.3) · [SHA-256](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.3/SHA256SUMS)

En Mac, descomprime y mueve GogaDownloader.app a Applications o a ~/Applications. En Windows, ejecuta el instalador por usuario. Para la actualización integrada de Windows se recomienda el instalador; la edición portable es una alternativa manual. No hay un paquete Mac Intel en esta release.

## Apertura más rápida en Mac

Mac **1.7.3** recupera las herramientas ya validadas sin repetir sus procesos de versión en cada apertura. Tras **15 días sin abrir**, revisa en segundo plano y permite seguir descargando. Si los ejecutables cambian, vuelve a validarlos. La primera preparación sí requiere una validación local.

Las consultas de versiones nuevas ocurren como máximo una vez cada 24 horas, también si falla la red; la revisión manual sigue disponible. Se corrigió además una espera que podía quedar bloqueada por un proceso hijo.

Mac 1.7.2 puede instalar desde Herramientas. Si una versión 1.7.0/1.7.1 muestra «El reinicio se canceló», cierra la app y reemplázala manualmente una vez con el ZIP. Se conservan preferencias, herramientas mutables y descargas.

**Windows conserva el comportamiento de 1.7.2** y se recompila con la versión nueva para mantener completo el feed compartido. La mejora de arranque de esta release corresponde a Mac.

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

Mac verificó cinco gestores nuevos y tres procesos independientes sin repetir probes, revisión tras 16 días de inactividad con una descarga activa, invalidación por cambios de archivo, un hijo que retenía la salida y el límite diario incluso con HTTP 503. Pasaron también las ocho suites habituales y una verificación final de la coordinación de revisiones pendientes.

Windows 1.7.3 pasó 167 checks con motores directos y 183 con motores comprimidos, build WinUI y auditoría del instalador. El instalador, portable y paquete de actualización se analizaron con Defender el 15 de octubre de 2026 sin detecciones; [consulta el informe con hashes](https://github.com/argokaz/gogadownloader-downloads/releases/download/v1.7.3/GogaDownloader-Windows-1.7.3-Defender-Scan.json). Esta release Windows no recibió una nueva instalación ni prueba de interfaz en la Ally.

Los motores mantienen los bytes auditados de las versiones anteriores. Las fuentes, recetas y avisos correspondientes se adjuntan a la release. No necesitas descargar esos archivos para usar la app; los feeds y nupkg son para el actualizador.

Los paquetes no tienen certificados comerciales. Mac usa firma ad hoc y no está notarizada; Windows no tiene firma Authenticode. La web explica el primer inicio en Mac. Los checksums verifican integridad; no se presentan como firma de un publisher ni como certificación antivirus.

Este repositorio distribuye las apps y los componentes de terceros. El código de desarrollo se mantiene en un repositorio privado.
