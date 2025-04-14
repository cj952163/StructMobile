graph LR
    subgraph Área Estratégica
        A[Definición y Revisión de Objetivos de Calidad] --> B(Planificación Estratégica de Pruebas);
        B --> C{Análisis del ROI en Pruebas};
        C -- Feedback & Métricas --> A;
    end

    subgraph Área Misional
        D["Desarrollo Guiado por Pruebas (TDD)"] --> E(Integración Continua / Entrega Continua (CI/CD));
        E --> F{Revisiones de Código & Pruebas de Pares};
        F --> G(Pruebas de Rendimiento & Carga);
        G --> H(Pruebas de Seguridad);
        H -- Resultados de Pruebas --> E;
        D -- Requisitos & Diseño --> E;
    end

    subgraph Área de Apoyo
        I[Gestión de Entornos de Prueba] --> J(Gestión de Datos de Prueba);
        J --> K(Selección y Mantenimiento de Herramientas de Prueba);
        K --> L{Análisis de Fallos & Lecciones Aprendidas};
        L -- Lecciones Aprendidas --> I;
        M[Recopilación y Análisis de Feedback] --> A;
        M --> L;
    end

    %% Interconexiones entre Áreas
    B -- Estrategia de Pruebas --> D;
    H -- Resultados de Seguridad --> L;
    E -- Necesidades de Infraestructura --> I;
    K -- Herramientas de Prueba --> D;
    K -- Herramientas de Prueba --> E;
    K -- Herramientas de Prueba --> F;
    K -- Herramientas de Prueba --> G;
    K -- Herramientas de Prueba --> H;
    L -- Lecciones Aprendidas --> A;
    L -- Lecciones Aprendidas --> B;
    L -- Lecciones Aprendidas --> D;
    L -- Lecciones Aprendidas --> E;
    L -- Lecciones Aprendidas --> K;
