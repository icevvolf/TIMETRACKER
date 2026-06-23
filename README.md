# TimeTracker ⏱️

App Android para registrar y gestionar horas extra, días festivos y descansos generados en el trabajo, con cálculo automático de balance acumulado.

Desarrollada en **Kotlin** con **Jetpack Compose**, pensada inicialmente para uso personal y de compañeros de trabajo en régimen de turnos.

---

## ✨ Funciones

### Gratis
- Registro de horas extra, días festivos, días de descanso y ajustes manuales
- Cálculo automático de balance acumulado (días / horas / minutos)
- Multiplicadores configurables por tipo de registro
- Historial completo de registros con edición y eliminación
- Exportación a PDF y JSON
- Importación de registros desde JSON
- Sistema de actualizaciones automáticas (descarga e instalación directa desde la app)

### Premium
- 🌙 Tema oscuro (de uso libre, no requiere premium)
- 🎨 Paletas de colores personalizables
- 📊 Gráficas de evolución mensual (horas generadas vs disfrutadas, con desglose de ajustes)
- 📅 Vista de calendario con registros por día
- 🔲 Widget de escritorio con balance y acceso rápido para añadir registros
- ☁️ Backup automático en Google Drive *(en desarrollo)*

La activación premium funciona mediante códigos: un código permanente y códigos promocionales con fecha de caducidad incrustada en el propio código.

---

## 🛠️ Stack técnico

- **Lenguaje:** Kotlin
- **UI:** Jetpack Compose + Material 3
- **Base de datos:** Room
- **Navegación:** Navigation Compose
- **Arquitectura:** MVVM (ViewModel + StateFlow)
- **Persistencia de preferencias:** SharedPreferences
- **Publicidad:** Google AdMob
- **Backup en la nube:** Google Drive API
- **Distribución:** GitHub Releases (versión beta) + sistema propio de comprobación de actualizaciones vía `version.json`

---

## 📂 Estructura del proyecto

```
com.tuapp.timetracker/
├── data/                        # Room: entidades y DAO
├── ui/
│   ├── screens/                 # Pantallas principales
│   │   └── premium/             # Pantallas y managers de funciones premium
│   └── theme/                   # Colores, tema oscuro, paletas
├── PreferenciasManager.kt        # Persistencia de configuración y premium
├── TimeTrackerViewModel.kt       # Lógica de negocio
├── VersionManager.kt             # Comprobación de actualizaciones
├── BackupManager.kt               # Exportación/importación JSON y PDF
├── TimeTrackerWidget.kt           # Widget de escritorio
└── MainActivity.kt
```

---

## 🚀 Compilación

1. Clona el repositorio
2. Ábrelo con Android Studio
3. Sincroniza Gradle
4. Conecta un dispositivo Android (minSdk 24) o usa un emulador
5. Run ▶️

No requiere configuración adicional para la versión gratuita. Las funciones de AdMob y Google Drive necesitan IDs propios configurados en `AndroidManifest.xml` y Google Cloud Console respectivamente.

---

## 📋 Estado del proyecto

🚧 **En desarrollo activo** — actualmente en fase de pruebas internas (beta) antes de su publicación en Google Play Store.

### Versión actual: 1.0.4

Distribución mediante APK directo con sistema de comprobación de actualizaciones automático (descarga e instalación gestionadas desde la propia app).

### Changelog reciente

- **v1.0.4** — Corregido cálculo de días festivos y descanso (ahora se aplica correctamente la conversión a horas según jornada configurada). Corregido orden de visualización de los últimos registros.
- **v1.0.3** — Descarga e instalación de actualizaciones directamente desde la app, sin pasar por el navegador.
- **v1.0.2** — Nuevo icono, widget de escritorio, gráficas mejoradas, banner de publicidad.

### Próximos pasos

- ☁️ Completar backup automático en Google Drive (login con Google Cloud Console pendiente)
- 🎯 Límite de horas anual según convenio, con alerta al superarlo
- 📤 Publicación en Google Play Store

---

## 📄 Licencia

Proyecto personal, de momento sin licencia pública definida.

---

*Desarrollado por [GusHi](https://github.com/icevvolf)*
