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
    B1 --> C(2. DASHBOARD / HOME (Resumen Operativo))

    %% Nivel 3: Pestañas Principales (Tab Bar Inferior)
    C --> D(2.1. Pestaña ÓRDENES DE SERVICIO/VEHÍCULOS)
    C --> E(2.2. Pestaña TAREAS / ACTIVIDADES)
    C --> F(2.3. Pestaña INVENTARIO / REPUESTOS)
    C --> H(2.4. Pestaña Notificaciones)
    C --> G(2.5. Pestaña Perfil / Configuración)

    %% Flujo D: Módulo Órdenes de Servicio (Proyectos)
    D --> D1(2.1.1. Lista de O/S (En Proceso, Espera))
    D1 --> D2(2.1.2. Detalle de O/S (Ver Vehículo/Cliente/Diagnóstico))
    D2 --> D3(2.1.3. Listado de Requisitos/Repuestos Necesarios)
    D2 --> D4(2.1.4. Historial de Mantenimiento)
    D1 -- Crear Nueva O/S --> D5(2.1.5. Crear/Seleccionar Cliente y Vehículo)
    D5 --> D2

    %% Flujo E: Módulo Tareas / Actividades
    E --> E1(2.2.1. Lista de Tareas Asignadas (Pendientes/Completadas))
    E1 --> E2(2.2.2. Detalle de Tarea (Registro de Horas/Materiales/Fotos))
    E1 --> E3(2.2.3. Crear Tarea Rápida)
    D2 -- Asignar Tarea --> E3

    %% Flujo F: Módulo Inventario / Repuestos (NUEVO)
    F --> F1(2.3.1. Consulta de Stock y Ubicación)
    F1 --> F2(2.3.2. Solicitud de Repuestos a Proveedor)
    F1 --> F3(2.3.3. Recepción de Repuestos (Actualizar Stock))

    %% Flujo H: Módulo Notificaciones (Anteriormente F)
    H --> H1(2.4.1. Historial de Notificaciones)
    H1 --> C

    %% Flujo G: Módulo Perfil / Configuración
    G --> G1(2.5.1. Mi Perfil (Ver/Editar Datos))
    G --> G2(2.5.2. Configuración de la App (Tema, Idioma))
    G --> G3(2.5.3. Cerrar Sesión)

    %% Conexiones
    E2 -- Tarea Completada --> E1
    G3 --> B

    %% Estilos para Usabilidad Móvil
    style C fill:#c7f3e1,stroke:#00a359,stroke-width:3px
    style D,E,F,H,G fill:#dae8fc,stroke:#6c8ebf
    style B1,B2,B3 fill:#e1d5e7,stroke:#9673a6
    style G3 fill:#f8cecc,stroke:#b85450

    
    ´´´
