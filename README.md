<h1 align="center">👋 ¡Hola! Soy Lisandro Semperez</h1>
<h3 align="center">🚀 Desarrollador .NET MAUI & Multiplataforma | C# | Arquitecturas Limpias</h3>

<p align="center">
  <a href="https://www.linkedin.com/in/lisandro-semperez-24b1782b8/">LinkedIn</a> •
  <a href="mailto:lisandrosemperez@gmail.com">Email</a> •
  <a href="https://github.com/lisandrosemperez-collab/AnotadorGymApp">Proyecto Destacado</a>
</p>

---

## 🧑‍💻 Sobre Mí

Desarrollador especializado en el ecosistema .NET, con un fuerte enfoque en crear **aplicaciones móviles multiplataforma nativas** usando .NET MAUI. Me apasiona implementar **arquitecturas limpias, código mantenible y experiencias de usuario fluidas**. 

A continuación, destaco mi proyecto principal, que sintetiza mi enfoque técnico y capacidad para llevar una aplicación a un estado funcional y pulido.

---

## 🏆 **Proyecto Destacado: Demostración de Habilidades**

### [🏋️ AnotadorGymApp - Aplicación MAUI Completa](https://github.com/lisandrosemperez-collab/AnotadorGymApp)
**Sistema profesional de tracking de entrenamientos que desarrollé desde cero.**

Este proyecto funciona como mi **carta de presentación técnica**, demostrando de manera práctica mis habilidades en:
- **Desarrollo Multiplataforma** con .NET MAUI y C#.
- **Arquitectura de Software** (Clean Architecture, MVVM, Repository Pattern).
- **Persistencia de Datos Avanzada** con SQLite y **Entity Framework Core**.
- **Optimización** y **Experiencia de Usuario** profesional.

---

## 🛠️ **Stack Tecnológico Principal**

### **💻 Desarrollo Multiplataforma**
![.NET MAUI](https://img.shields.io/badge/.NET_MAUI-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white)
![XAML](https://img.shields.io/badge/XAML-0C54C2?style=for-the-badge&logo=xaml&logoColor=white)

### **🗄️ Bases de Datos & Persistencia**
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)
![Entity Framework Core](https://img.shields.io/badge/Entity_Framework_Core-512BD4?style=for-the-badge&logo=dotnet&logoColor=white)
![JSON](https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white)

### **📊 Visualización de Datos**
![Microcharts](https://img.shields.io/badge/Microcharts-FF6F00?style=for-the-badge)
![Charts](https://img.shields.io/badge/Data_Visualization-4285F4?style=for-the-badge)

---

## ⚙️ **Características Técnicas Avanzadas Implementadas**

### **🏗️ Arquitectura & Patrones**
- **Inyección de Dependencias** - Servicios modularizados y testables
- **Patrón Repository** - Separación clara entre lógica de negocio y datos
- **Servicios Especializados:**
  - `DataService` - Gestión de operaciones CRUD complejas
  - `ConfigService` - Manejo centralizado de configuraciones
  - `ImageService` - Carga y cache de imágenes optimizada
- **Clean Architecture** - Separación en capas claramente definidas

### **📱 Experiencia de Usuario Premium**
- **Splash Screen Inteligente** con ProgressBar que muestra:
  - Inicialización de base de datos
  - Carga de datos desde JSON
  - Verificación de integridad de datos
- **Tema Claro/Oscuro** implementado globalmente
  - Cambio en tiempo real sin reiniciar la app
  - Persistencia de preferencias del usuario
- **UI/UX optimizada** para diferentes tamaños de pantalla

### **🗄️ Gestión de Datos Profesional**
- **Base de datos SQLite con Entity Framework Core** - ORM completo para mapeo objeto-relacional
- **Sistema de seeding desde JSON** - Poblado automático inicial usando migraciones EF Core
- **Code-First Development** - Modelo de dominio define el esquema de base de datos
- **Relaciones complejas mapeadas por EF Core:**
  - Ejercicios ↔ Rutinas
  - Historial de entrenamientos
  - Progreso del usuario
- **Optimización de consultas** con LINQ y configuraciones específicas de EF Core

### **📊 Métricas & Analytics**
- **Gráficos interactivos** con Microcharts
- **Estadísticas en tiempo real**
- **Seguimiento de progreso** histórico
- **Exportación de datos**

---

## 🏗️ **Arquitectura del Proyecto**

La aplicación sigue el patrón **Model-View-ViewModel (MVVM)** y está organizada en una estructura modular centrada en páginas y funcionalidades, lo que facilita la navegación y el mantenimiento del código.

```csharp
AnotadorGymApp/ # 🎨 CAPA DE PRESENTACIÓN (App .NET MAUI)
│
├── AppShell.xaml (.cs) # Navegación principal con Shell
├── MauiProgram.cs # Configuración e Inyección de Servicios
│
├── 📱 Páginas (Vistas y Lógica de UI)
│ ├── MainPage/
│ │ ├── MainPage.xaml (.cs) # Vista principal (Dashboard)
│ │ ├── SplashPage.xaml (.cs) # Pantalla de inicio con ProgressBar
│ │ └── ResumenSemanal.cs # Modelo/VistaModelo para resumen
│ │
│ ├── RutinasPage/
│ │ ├── PrincipalRutinasPage.xaml (.cs) # Vista lista de rutinas
│ │ ├── AgregarRutinaPage.xaml (.cs) # Vista creación/edición
│ │ └── ComienzoRutinaPage.xaml (.cs) # Vista detalle y ejecución
│ │
│ ├── MetricasPage/
│ │ └── MetricasPage.xaml (.cs) # Vista de gráficos y estadísticas
│ │
│ ├── ConfiguracionPage/
│ │ └── ConfigPage.xaml (.cs) # Vista de ajustes y tema
│ │
│ ├── RegistroEjercicios/ # Lógica para métricas
│ │ ├── ChartsService.cs # Servicio de generación de gráficos
│ │ └── EjercicioConMetricas.cs # Modelo para métricas
│ │
│ └── PopUp/
│ └── BuscarEjerciciosPopUp.xaml (.cs) # Diálogo modal reutilizable
│
├── 🛠️ Servicios de Aplicación
│ ├── ConfigService.cs # Gestión de configuración y preferencias
│ └── ImagenPersistenteService.cs # Manejo y persistencia de imágenes
│
└── 🎨 Recursos
├── Styles/
│ ├── Styles.xaml (.cs) # Estilos base
│ ├── LightTheme.xaml (.cs) # Tema claro (implementación dinámica)
│ └── DarkTheme.xaml (.cs) # Tema oscuro (implementación dinámica)
│
├── Images/
│ ├── [iconos].png # Iconos de la aplicación
│ └── RutinasImages/
│ └── [rutinas].jpg # Imágenes predefinidas para rutinas
│
├── Fonts/ # Fuentes personalizadas (.otf, .ttf)
└── Raw/
└── Ejercicios.json # Base de datos semilla (+1000 ejercicios)

AnotadorGymApp.Data/ # 💾 CAPA DE DOMINIO Y DATOS (Librería .NET)
│
├── 💾 DataService.cs # REPOSITORIO PRINCIPAL
│ # - Implementa el Patrón Repository
│ # - Gestión CRUD completa usando Entity Framework Core
│ # - Carga optimizada por lotes desde JSON
│ # - Caché en memoria y configuración SQLite (WAL mode)
│
├── 🗃️ Entidades (Modelo de Dominio)
│ ├── Rutinas.cs # Entidad principal de rutina (mapeada por EF Core)
│ ├── Exercise.cs # Entidad de ejercicio (mapeada por EF Core)
│ └── Muscles.cs # Entidad para clasificación muscular (mapeada por EF Core)
│
├── 📄 DTOs y Modelos de Persistencia
│ └── ExerciseJson.cs # Modelo para deserialización del JSON
│
└── 🗄️ DataBase.cs (DbContext) # Contexto de EF Core para SQLite
└── Migrations/ # Historial de migraciones automáticas de EF Core
```

### **🗄️ Persistencia con Entity Framework Core**
La capa de datos utiliza **Entity Framework Core 8** con el proveedor **SQLite**. Esta elección permite:
- **Enfoque Code-First**: Las entidades de dominio (`Rutinas`, `Exercise`) definen el esquema de la base de datos.
- **Migraciones automáticas**: La carpeta `Migrations/` contiene el historial de cambios en el esquema, gestionado por EF Core.
- **Consultas LINQ integradas** y manejo eficiente de relaciones (como `Rutina ↔ Exercise`).
- **Configuración de rendimiento** (como el modo WAL) aplicada a través del `DbContext`.

### **🔧 Flujo y Comunicación entre Capas**

1.  **Inicio y Configuración**: `MauiProgram.cs` registra y construye los servicios (`DataService`, `ConfigService`) que se inyectan en las páginas.
2.  **Presentación (MVVM)**: Las **Vistas** (`*.xaml`) usan **Data Binding** para conectarse a la lógica en sus **Code-Behind/Vistas-Modelo** (`*.xaml.cs`, `ResumenSemanal.cs`).
3.  **Lógica de Negocio**: Las páginas y servicios de la UI consumen el `DataService`, que actúa como un **Único Punto de Acceso** (Facade/Repository) a todos los datos.
4.  **Persistencia**: El `DataService` utiliza el `DataBase` (DbContext de EF Core) para realizar operaciones **CRUD** en la base de datos SQLite, aprovechando el mapeo objeto-relacional, **LINQ** y las migraciones.
5.  **Separación Física**: La capa de datos es un **proyecto de librería de clase separado** (`AnotadorGymApp.Data.csproj`), forzando una dependencia unidireccional y limpia.

**Esta estructura refleja fielmente tu implementación y destaca las decisiones técnicas maduras que ya has tomado, como la separación de proyectos y el uso del patrón Repository.**

### **🎨 Características de UI/UX**
## Temas Implementados
```xml
<!-- Sistema de temas dinámicos -->
<ResourceDictionary Source="{AppThemeBinding Light=LightTheme.xaml,
                                              Dark=DarkTheme.xaml}" />

<!-- Uso en toda la aplicación -->
<Label Text="Bienvenido" 
       TextColor="{DynamicResource PrimaryTextColor}" />
```

## **Servicios de Imágenes**

- Loading states con placeholders

- Optimización para diferentes resoluciones

- Fallback a imágenes por defecto

## **🔮 Roadmap & Mejoras Futuras**
### **✅ COMPLETADO**
- Base de datos con seeding desde JSON

- Sistema de temas claro/oscuro

- Métricas con gráficos

- Inyección de dependencias

- Servicios modularizados

### **🚧 EN PROGRESO**
- Sincronización en la nube

- Backup/restore de datos

- Compartir rutinas

### **📅 PLANIFICADO**
- IA para sugerencias de rutinas

- Integración con wearables

## **📫 Conectemos**
<p align="center"> <a href="https://www.linkedin.com/in/lisandro-semperez-24b1782b8/"> <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/> </a> <a href="mailto:lisandrosemperez@gmail.com"> <img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/> </a> <a href="https://github.com/lisandrosemperez-collab/AnotadorGymApp"> <img src="https://img.shields.io/badge/Ver_Proyecto_Completo-GitHub-black?style=for-the-badge&logo=github" alt="GitHub"/> </a> </p>

<p align="center"> <i>"Convierto café en código, y problemas en soluciones elegantes."</i><br> <sub>Buscando oportunidades para crear aplicaciones que impacten positivamente.</sub> </p>
