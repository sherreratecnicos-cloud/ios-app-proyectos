# iOS CI con GitHub Actions

Este repositorio está configurado para compilar y testear la app automáticamente usando GitHub Actions.

## 🚀 Cómo funciona
- Al hacer `push` o abrir un `pull request` en `main` o `develop`:
  - Compila la app con Xcode.
  - Ejecuta los tests unitarios en un simulador.
  - Genera un archivo `.xcarchive` y un `.ipa`.
  - Sube el resultado como *artifact* descargable en la pestaña de Actions.

## 🔧 Configuración
1. Cambia `YourAppScheme` y `YourApp.xcodeproj` en `.github/workflows/ios-build.yml`.
2. Si usas CocoaPods, reemplaza `-project` por `-workspace`.
3. Descarga el `.ipa` desde GitHub Actions → tu workflow → Artifacts.
