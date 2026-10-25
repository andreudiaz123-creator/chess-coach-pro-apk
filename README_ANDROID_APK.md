# Chess Coach Pro — Proyecto Android (.APK) y PWA

Este paquete contiene todo lo necesario para instalar y compilar **Chess Coach Pro** como una aplicación nativa de Android (`.apk`).

## ¿Por qué se entrega este paquete listo para compilar?
El entorno de ejecución en la nube donde se genera el código no incluye el SDK binario de Android (`aapt2` / `android.jar` / `d8`) por restricciones de seguridad del contenedor, pero he dejado **todo el proyecto Android nativo ensamblado** junto con un flujo de compilación automática en la nube.

---

## Método 1: Compilar el archivo `.APK` gratis en la nube (Sin instalar nada en tu PC)

1. Crea un repositorio nuevo en [GitHub](https://github.com/new) y sube el contenido descomprimido de este archivo ZIP.
2. Ve a la pestaña **Actions** de tu repositorio en GitHub.
3. El flujo automático **«Compilar APK de Chess Coach Pro»** (`.github/workflows/build-apk.yml`) se ejecutará solo y en ~2 minutos generará el archivo **`app-debug.apk`** firmado y listo para instalar en tu teléfono Android.
4. Descárgalo desde la sección **Artifacts** (`ChessCoachPro-Android-APK`) e instálalo en tu móvil.

---

## Método 2: Compilar el `.APK` en tu ordenador con Android Studio

1. Descomprime este archivo ZIP en una carpeta.
2. Abre **Android Studio** y selecciona **Open** eligiendo la carpeta descomprimida.
3. En el menú superior, haz clic en **Build → Build Bundle(s) / APK(s) → Build APK(s)**.
4. El archivo `.apk` se generará en `app/build/outputs/apk/debug/app-debug.apk`.

---

## Método 3: Instalar directamente en Android sin compilar (Modo PWA)

La aplicación `app/src/main/assets/www/index.html` (también abierta en tu vista previa principal como `chess_coach_pro.html`) tiene soporte **PWA (Progressive Web App)**:
1. Ábrela desde **Google Chrome** en tu teléfono Android.
2. Toca el botón de menú **⋮** (esquina superior derecha) y elige **«Añadir a pantalla de inicio»** o **«Instalar aplicación»**.
3. Quedará instalada con su icono en tu cajón de aplicaciones y se ejecutará a pantalla completa sin barras del navegador.
