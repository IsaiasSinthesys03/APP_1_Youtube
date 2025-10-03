# FlutterDev Playlists

**Una aplicación Flutter moderna para explorar y reproducir listas de reproducción de YouTube con interfaz adaptativa**

## 📜 Descripción General

FlutterDev Playlists es una aplicación móvil y web desarrollada en Flutter que permite a los usuarios explorar y reproducir listas de reproducción del canal oficial de Flutter en YouTube. La aplicación se conecta directamente con la YouTube Data API v3 para obtener información en tiempo real de las listas de reproducción y sus videos.

La aplicación está diseñada con un enfoque en la experiencia de usuario adaptativa, proporcionando diferentes interfaces según el tamaño de pantalla y la plataforma. En dispositivos móviles y pantallas pequeñas, utiliza una navegación por pestañas, mientras que en pantallas más grandes (tablets y escritorio) presenta una vista dividida que permite ver las listas y los detalles simultáneamente.

## ✨ Características Principales

* **Interfaz Adaptativa:** Se ajusta automáticamente entre vista móvil y de escritorio según el tamaño de pantalla
* **Integración con YouTube API:** Conexión directa con la YouTube Data API v3 para obtener datos en tiempo real
* **Navegación Intuitiva:** Sistema de navegación fluido con GoRouter para una experiencia de usuario moderna
* **Reproducción Externa:** Enlaces directos a YouTube para reproducir videos en la plataforma oficial
* **Diseño Material 3:** Implementación completa del sistema de diseño Material 3 con temas claro y oscuro
* **Gestión de Estado:** Uso de Provider para un manejo eficiente del estado de la aplicación
* **Soporte Multiplataforma:** Compatible con Android, iOS, Web, Windows, macOS y Linux
* **Vista Dividida:** En pantallas grandes, permite ver listas y detalles de videos simultáneamente
* **Carga Paginada:** Implementación eficiente de paginación para manejar grandes cantidades de contenido

## 🛠️ Tecnologías Utilizadas

* **Frontend:**
  * Flutter 3.8.1+ (Framework principal)
  * Dart (Lenguaje de programación)
  * Material Design 3 (Sistema de diseño)
  * FlexColorScheme (Temas personalizados)

* **Navegación y Estado:**
  * GoRouter 16.2.4 (Navegación declarativa)
  * Provider 6.1.5+1 (Gestión de estado)

* **Integración Externa:**
  * YouTube Data API v3 (Google APIs 15.0.0)
  * HTTP 1.5.0 (Comunicación con APIs)
  * URL Launcher 6.3.2 (Apertura de enlaces externos)

* **UI/UX:**
  * Split View 3.2.1 (Vista dividida para pantallas grandes)
  * Responsive Design (Diseño adaptativo)

* **Herramientas de Desarrollo:**
  * Flutter Lints 5.0.0 (Análisis de código)
  * Git (Control de versiones)
  * Flutter SDK 3.8.1+

## 🚀 Cómo Empezar

### **Prerrequisitos**

Antes de comenzar, asegúrate de tener instalado:

* [Flutter SDK](https://flutter.dev/docs/get-started/install) (versión 3.8.1 o superior)
* [Dart SDK](https://dart.dev/get-dart) (incluido con Flutter)
* [Git](https://git-scm.com/) (para clonar el repositorio)
* Un editor de código (recomendado: [Visual Studio Code](https://code.visualstudio.com/) con la extensión Flutter)
* [Android Studio](https://developer.android.com/studio) (para desarrollo Android)
* [Xcode](https://developer.apple.com/xcode/) (para desarrollo iOS, solo en macOS)

### **Configuración de la YouTube API**

**⚠️ IMPORTANTE:** Antes de ejecutar la aplicación, necesitas configurar tu propia clave de API de YouTube:

1. Ve a [Google Cloud Console](https://console.cloud.google.com/)
2. Crea un nuevo proyecto o selecciona uno existente
3. Habilita la YouTube Data API v3
4. Crea credenciales (API Key)
5. Reemplaza la clave en `lib/main.dart`:

```dart
// Reemplaza esta línea en lib/main.dart
const youTubeApiKey = 'TU_CLAVE_DE_API_AQUI';
```

### **Instalación**

1. **Clona el repositorio:**
   ```bash
   git clone https://github.com/IsaiasSinthesys03/APP_1_Youtube.git
   ```

2. **Navega al directorio del proyecto:**
   ```bash
   cd APP_1_Youtube
   ```

3. **Instala las dependencias:**
   ```bash
   flutter pub get
   ```

4. **Configura la API Key de YouTube:**
   Edita el archivo `lib/main.dart` y reemplaza la variable `youTubeApiKey` con tu clave de API.

### **Ejecución**

* **Para ejecutar en modo de desarrollo:**
  ```bash
  flutter run
  ```

* **Para ejecutar en una plataforma específica:**
  ```bash
  # Android
  flutter run -d android
  
  # iOS (solo en macOS)
  flutter run -d ios
  
  # Web
  flutter run -d web-server --web-port 8080
  
  # Windows
  flutter run -d windows
  
  # macOS
  flutter run -d macos
  
  # Linux
  flutter run -d linux
  ```

* **Para construir la aplicación:**
  ```bash
  # Android APK
  flutter build apk
  
  # Android App Bundle
  flutter build appbundle
  
  # iOS
  flutter build ios
  
  # Web
  flutter build web
  
  # Windows
  flutter build windows
  
  # macOS
  flutter build macos
  
  # Linux
  flutter build linux
  ```

Una vez ejecutado, la aplicación se abrirá en tu dispositivo/emulador. En web, visita `http://localhost:8080` (o el puerto que especifiques).

## 📂 Estructura del Proyecto

```
/
├── lib/                          # Código fuente principal de Flutter
│   ├── main.dart                 # Punto de entrada de la aplicación
│   └── src/                      # Módulos de la aplicación
│       ├── adaptive_playlists.dart    # Lógica de interfaz adaptativa
│       ├── app_state.dart            # Gestión de estado y API de YouTube
│       ├── playlist_details.dart     # Vista de detalles de videos
│       └── playlists.dart            # Lista de reproducciones
├── android/                     # Configuración específica de Android
│   ├── app/
│   │   └── build.gradle.kts     # Configuración de build para Android
│   └── ...
├── ios/                         # Configuración específica de iOS
│   ├── Runner/
│   │   └── Info.plist           # Configuración de la app iOS
│   └── ...
├── web/                         # Configuración para web
│   ├── index.html               # Página principal HTML
│   ├── manifest.json            # Manifest de la PWA
│   └── icons/                   # Iconos para web
├── windows/                     # Configuración para Windows
├── macos/                       # Configuración para macOS
├── linux/                       # Configuración para Linux
├── pubspec.yaml                 # Dependencias y metadatos del proyecto
├── pubspec.lock                 # Versiones exactas de dependencias
└── README.md                    # Esta documentación
```

### **Descripción de Componentes Principales:**

* **`main.dart`:** Configuración de la aplicación, rutas, temas y punto de entrada
* **`app_state.dart`:** Clase principal que maneja el estado, conexión con YouTube API y caché de datos
* **`adaptive_playlists.dart`:** Lógica para determinar si mostrar vista móvil o de escritorio
* **`playlists.dart`:** Widget que muestra la lista de reproducciones disponibles
* **`playlist_details.dart`:** Widget que muestra los videos de una lista de reproducción específica

## 📝 Contribuciones

¡Las contribuciones son bienvenidas! Si quieres contribuir al proyecto:

1. **Fork** el repositorio
2. **Crea** una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. **Commit** tus cambios (`git commit -m 'Agrega nueva funcionalidad'`)
4. **Push** a la rama (`git push origin feature/nueva-funcionalidad`)
5. **Abre** un Pull Request

### **Áreas de Mejora Sugeridas:**

* Implementación de caché local para videos
* Soporte para múltiples canales de YouTube
* Funcionalidad de búsqueda
* Modo offline
* Notificaciones push
* Mejoras en la accesibilidad
* Tests unitarios y de integración

---

**Desarrollado con ❤️ usando Flutter**
