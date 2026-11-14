# FocoUC para Android

Este proyecto envuelve la app FocoUC (HTML, CSS y JavaScript) dentro de una app Android. El APK que genera se instala en cualquier celular Android 7.0 o superior.

## Opción A: sin instalar nada (GitHub, unos 5 minutos)

1. Crea una cuenta gratis en github.com y un repositorio nuevo, por ejemplo `focouc`.
2. Sube **todo el contenido de esta carpeta** al repositorio (botón *Add file → Upload files*). Importante: la carpeta oculta `.github` también debe subirse. Si tu navegador no deja arrastrarla, sube el zip descomprimido con GitHub Desktop o desde la terminal con `git`.
3. Entra a la pestaña **Actions**. El flujo «Construir APK de FocoUC» se ejecuta solo. Si no, ábrelo y pulsa **Run workflow**.
4. Cuando termine (3 a 6 minutos, círculo verde), abre la ejecución y descarga **FocoUC-apk** al final de la página. Es un zip que contiene `app-debug.apk`.
5. Pasa el APK al celular (cable, Drive o WhatsApp a ti mismo).

## Opción B: con Android Studio

1. Instala Android Studio (gratis) y usa *Open* sobre esta carpeta.
2. Espera a que termine la sincronización de Gradle.
3. Menú **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
4. El archivo queda en `app/build/outputs/apk/debug/app-debug.apk`.

## Instalar en el celular

1. Abre el APK desde el administrador de archivos.
2. Android pedirá permiso para **instalar apps de esta fuente** (Chrome, Archivos o WhatsApp). Actívalo solo para instalar.
3. Pulsa **Instalar**. Si Play Protect avisa que la app no es conocida, es normal en un APK de prueba: elige *Instalar de todos modos*.

## Qué hace y qué no hace esta versión

- Funciona sin internet: Pomodoro, bosque, calendario, plan si-entonces, microlecciones y los 4 niveles de alerta. Tus datos se guardan en el celular.
- Las tipografías se descargan de Google Fonts cuando hay internet. Sin conexión se usa la tipografía del sistema.
- Las alertas aparecen **mientras la app está abierta**. Las notificaciones con la app cerrada y el bloqueo real de otras apps requieren servicios nativos de Android (alarmas exactas, UsageStats, servicio en primer plano). Eso es la siguiente etapa del proyecto.
- El nivel 4 se demuestra en el «teléfono de prueba» dentro de la app, no bloquea apps reales.

## Ajustes útiles

- Cambiar el nombre o el paquete: `app/build.gradle` (`applicationId`) y `app/src/main/res/values/strings.xml`.
- Cambiar el contenido de la app: `app/src/main/assets/index.html`.
- Cambiar el ícono: reemplaza los `ic_launcher.png` de las carpetas `app/src/main/res/mipmap-*`.
