# MapaDeNavegacionMovil
´´´mermaid
    graph TD
    %% Nivel 0: Inicio de la Aplicación
    A[0. Inicio / Splash Screen] --> B(1. Autenticación)

    %% Nivel 1: Autenticación
    B --> B1{1.1. Login (Inicio Sesión)}
    B --> B2{1.2. Registro (Nuevo Usuario)}
    B --> B3{1.3. Recuperar Contraseña}

    %% Nivel 2: Navegación Principal (Tras el Login Exitoso)
    B1 --> C(2. DASHBOARD / HOME (Main Tab Bar))

    %% Nivel 3: Pestañas Principales (Tab Bar Inferior)
    C --> D(2.1. Pestaña Proyectos)
    C --> E(2.2. Pestaña Tareas / Actividades)
    C --> F(2.3. Pestaña Notificaciones)
    C --> G(2.4. Pestaña Perfil / Configuración)

    %% Flujo D: Módulo Proyectos
    D --> D1(2.1.1. Lista de Proyectos)
    D1 --> D2(2.1.2. Detalle de Proyecto)
    D2 --> D3(2.1.3. Gestión de Requisitos (Lista/Creación))
    D2 --> D4(2.1.4. Progreso / Reportes Breves)

    %% Flujo E: Módulo Tareas / Actividades
    E --> E1(2.2.1. Lista de Tareas Asignadas)
    E1 --> E2(2.2.2. Detalle de Tarea (Cambio de Estado))
    E1 --> E3(2.2.3. Crear Nueva Tarea)

    %% Flujo F: Módulo Notificaciones
    F --> F1(2.3.1. Historial de Notificaciones)
    F1 --> C

    %% Flujo G: Módulo Perfil / Configuración
    G --> G1(2.4.1. Mi Perfil (Ver/Editar Datos))
    G --> G2(2.4.2. Cambiar Contraseña)
    G --> G3(2.4.3. Configuración de la App (Tema, Idioma, Accesibilidad))
    G --> G4(2.4.4. Cerrar Sesión)

    %% Conexiones
    D1 -- Nueva Tarea --> E3
    D3 -- Volver --> D2
    E2 -- Tarea Completada --> E1
    G4 --> B

    %% Estilos para Usabilidad Móvil
    style C fill:#c7f3e1,stroke:#00a359,stroke-width:3px
    style D,E,F,G fill:#dae8fc,stroke:#6c8ebf
    style B1,B2,B3 fill:#e1d5e7,stroke:#9673a6
    style G4 fill:#f8cecc,stroke:#b85450
    
    ´´´
