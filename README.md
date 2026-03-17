# 🎹 piaananum

Proyecto académico **PIA** (Proyecto Integrador de Aprendizaje) desarrollado con **Flutter Web**. Aplicación web interactiva que corre directamente en el navegador sin necesidad de instalación.

---

## 📌 Descripción

**piaananum** es una aplicación web construida con Flutter como proyecto integrador. Compila a WebAssembly/JavaScript y se sirve como sitio estático, aprovechando el motor de renderizado CanvasKit para una experiencia visual consistente en todos los navegadores modernos.

---

## 🚀 Tecnologías

| Tecnología | Descripción |
|------------|-------------|
| [Flutter](https://flutter.dev/) | Framework principal (Web) |
| Dart | Lenguaje de programación |
| CanvasKit / SkWasm | Motor de renderizado gráfico |
| PWA | Soporte como Progressive Web App |

---

## 📁 Estructura del proyecto

```
piaananum/
├── index.html                  # Punto de entrada de la app
├── main.dart.js                # Código compilado de Flutter
├── flutter.js                  # Inicializador del motor Flutter
├── flutter_service_worker.js   # Service Worker para PWA
├── manifest.json               # Manifiesto de la Web App
├── favicon.png                 # Ícono del sitio
├── assets/                     # Fuentes y recursos estáticos
├── canvaskit/                  # Motor de renderizado (CanvasKit + SkWasm)
└── icons/                      # Íconos para PWA (192x192, 512x512)
```

---

## 🌐 Ejecutar localmente

Flutter Web requiere ser servido desde un servidor HTTP. No abras `index.html` directamente con doble clic.

### Opción 1 — Python

```bash
cd piaananum/
python3 -m http.server 8080
```

Abre en el navegador: [http://localhost:8080](http://localhost:8080)

### Opción 2 — Node.js (`serve`)

```bash
npx serve piaananum/
```

### Opción 3 — VS Code

Instala la extensión **Live Server** y abre `index.html` con ella.

---

## ☁️ Despliegue en producción

Al ser un build estático de Flutter Web, es compatible con cualquier hosting estático:

- **GitHub Pages** — Sube el contenido al branch `gh-pages`
- **Netlify / Vercel** — Arrastra la carpeta al dashboard
- **Firebase Hosting** — Apunta la carpeta `public` a este directorio y ejecuta `firebase deploy`

---

## 🛠️ Sobre el build

Este repositorio contiene el **build de producción** generado con:

```bash
flutter build web --release
```

Para modificar o desarrollar desde el código fuente se necesita el proyecto Dart original y Flutter instalado:

```bash
# Verificar instalación
flutter --version   # Flutter 3.x o superior recomendado
dart --version

# Instalar dependencias
flutter pub get

# Correr en modo desarrollo
flutter run -d chrome

# Generar build de producción
flutter build web --release
```

---

## 📱 PWA

La aplicación está configurada como **Progressive Web App** y puede instalarse en dispositivos móviles y de escritorio directamente desde el navegador (Chrome / Edge → "Instalar aplicación").

---

## 👥 Autores

Proyecto desarrollado como parte del **PIA** (Proyecto Integrador de Aprendizaje).

---

## 📄 Licencia

MIT — libre para usar, modificar y distribuir.
