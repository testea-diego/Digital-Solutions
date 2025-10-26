# Rediseño Sitio Web Digital Solutions
## Plan de Pruebas

1. ### Antecedentes

    1. #### Contexto del Proyecto:

        Digital Solutions, empresa líder en soluciones tecnológicas, ha contratado nuestros servicios para liderar los esfuerzos de calidad y asegurar la exitosa creación y lanzamiento de su nuevo sitio web. Este proyecto representa una iniciativa estratégica para modernizar su presencia digital, mejorar la experiencia de usuario y consolidar su posición en el mercado.

    2. #### Alcance del Rediseño:
    
        El proyecto engloba el rediseño completo del sitio web existente, comenzando con las páginas consideradas componentes críticos. La nueva implementación busca:
        
        - Implementar un diseño moderno y responsive según especificaciones de Figma.
        - Mantener la integridad del contenido existente mientras se mejora la presentación.
        - Garantizar la compatibilidad cross-browser y multi-dispositivo.
        - Establecer las bases para futuras expansiones del sitio.

    3. #### Objetivos de Calidad:
    
        Como equipo de QA, nuestros objetivos principales son:

        - Validar la fidelidad del diseño frente a los mockups de Figma.
        - Asegurar la funcionalidad responsive en todos los dispositivos target.
        - Verificar la preservación del contenido y funcionalidades existentes en el sitio actual.
        - Establecer procesos de testing escalables para fases futuras del proyecto.

    4. #### Metodología:

        Trabajando bajo un enfoque ágil, implementaremos:
        - Sprint-based testing integrado con el desarrollo iterativo.
        - Definition of Done claras en cada User Story.
        - Continuous feedback entre desarrollo y QA.
        - Risk-based testing priorizando componentes críticos del negocio.


2. ### Objetivos

    1. #### Calidad del producto:

        - Garantizar el 100% de cumplimiento con los diseños de Figma en todos los breakpoints definidos.
        - Asegurar el 99% de funcionalidad cross-browser en los navegadores objetivo.
        - Mantener el 100% de integridad del contenido textual en relación a la versión anterior del sitio.
        - Mantener los defectos críticos en producción por debajo del 1% del total de issues identificados.
    
    2. #### Cobertura de Testing:

        - Ejecutar el 100% de los casos de prueba definidos para cada User Story antes del release.
        - Alcanzar 75% de cobertura en dispositivos móviles definidos en el **Documento de Compatibilidad**.
        - Validar el 100% de los componentes responsive en los todos los breakpoints críticos (**Documento de Compatibilidad**).
        - 100% de los Criterios de Aceptación cubiertos por casos de prueba.
    
    3. #### Métricas de Calidad Específicas:

        - Cero defectos bloqueantes en ambiente de producción post-release.
        - Tasa de éxito mayor al 98% en pruebas de regresión por sprint.
        - 100% de los Criterios de Aceptación verificados y aprobados por PO.
        - Cumplimiento con los criterios definidos en el **Documento de SEO**, en relación a Web Vitals Core, score en Lighthouse y los tiempos de carga del sitio.
    
    4. #### Comunicación, Transparencia, Reportes:

        - Mantener actualizados en tiempo real todos los boards y métricas del proyecto, así proveer de información de calidad al leadership team.
        - Realizar al menos 1 sesión de Test Review por Sprint con el equipo de leadership y/o desarrollo.
        - 100% de participación en ceremonias ágiles (daillies, plannings, retrospectives, grooming).

3. ### Gestión de Riesgos

    1. #### Identificación de Riesgos y Matriz de Priorización

        - Se creará un documento **Gestión de Riesgos** donde se identificarán los riesgos principales (técnicos y de proceso) y se generará una matriz priorizada, a partir de su impacto y probabilidad de ocurrencia; responsabilidades y métodos de mitigación.
        - El plan documentado será revisado y actualizado al final de cada Sprint, o cuando se identifiquen nuevos riesgos durante el proceso de desarrollo.
    
    2. #### Plan de Mitigación Proactiva

        - Establecer ambientes de prueba estables, con data clonada de producción.
        - Definir y documentar los breakpoints responsivos.
        - Uso de granjas de dispositivos (como BrowserStack) y testing en dispositivos reales.
        - Mapeo temprano de dependencias.
        - Definir con claridad los criterios de entrada y salida para todos los ítems de trabajo.
        - Creación y mantenimiento activo de la suite de casos de regresión.
        - Creación y mantenimiento de una sub-suite de casos automatizados.

4. ### Estrategia de Testing

    1. #### Estrategia Shift-Left

        - Integración Temprana en el Ciclo de Desarrollo
            - Diseño de casos de prueba en paralelo al desarrollo de cada User Story.
            - Participación de QA en refinamiento de historias para identificar criterios de aceptación testeables.
            - Review colaborativo de especificaciones entre desarrolladores, QA y diseñadores.

    2. #### Actividades por Fase del Sprint:

        - Fase de Planificación (Sprint Planning)
            - Análisis de requerimientos y criterios de aceptación.
            - Identificación de dependencias y riesgos.
            - Estimación de esfuerzo de pruebas para cada historia.
        - Fase de Desarrollo
            - Diseño detallado de casos de prueba.
            - Preparación de datos de prueba y ambiente.
            - Comunicación continua con desarrolladores sobre progreso.
        - Fase de Testing
            - Ejecución de pruebas funcionales y visuales.
            - Reporte temprano de defectos.
            - Testeo y retesteo de defectos / fixes.

    3. #### Pirámide de Testing

        - **Nivel 1:** Tests Unitarios - Responsabilidad: Equipo de Desarrollo
            - Cobertura mínima del 80% para componentes críticos
            - Ejecución en pipeline de CI/CD en cada commit
            - Criterio de aceptación: cero bugs por funcionalidad básica
        - **Nivel 2:** Tests de Integración - Responsabilidad: QA + Desarrollo
            - Validación de APIs y servicios usando Postman
            - Collections de Postman para endpoints críticos
            - Monitoreo de performance de servicios backend
        - **Nivel 3:** Tests UI / E2E / Visual - Responsabilidad: Equipo de QA
            - Tests E2E críticos con Playwright
            - Validación cross-browser en navegadores objetivo
            - Pruebas de responsive design en dispositivos virtuales y reales
            - Pruebas UX/UI subjetivas (diseño visual, usabilidad, experiencia)
            - Pruebas exploratorias y ad-hoc
    
    4. #### Estrategia de Automatización:
    
        Criterios para Identificación de Casos Automatizables

        1. Alta Prioridad para Automatización
            - Flujos críticos de negocio (login, navegación principal, búsquedas)
            - Pruebas de regresión ejecutadas en cada release
            - Validación cross-browser en múltiples configuraciones
            - Pruebas de datos con múltiples conjuntos de entrada
        2. Media Prioridad para Automatización
            - Pruebas de integración entre componentes
            - Validación de formularios con diferentes estados
            - Pruebas de performance básicas

    5. #### Plan de Implementación de Automatización:

        - **Sprints 1 - 2**
            - Setup de frameworks de automatización
            - Automatización de smoke tests para Home
            - Collections de Postman para APIs existentes
        - **Sprints 3 - 4**
            - Expansión de regresión visual para componentes clave
            - Automatización de flujos críticos de usuario
            - Integración en pipeline CI/CD
        - **Sprints 5+**
            - Aumento de cobertura de regresión para releases
            - Dashboard de reporting automatizado
            - Optimización de tiempos de ejecución

5. ### Criterios de Entrada / Salida

    1. ### Criterio de Entrada - Definition of Ready (DOR)

        - **Para User Stories**
            - Requisitos claros y específicos: US con descripción detallada y criterios de aceptación definidos y testeables
            - Diseños completos: Mockups de Figma disponibles y aprobados para todos los breakpoints
            - Datos de prueba: Conjuntos de datos necesarios identificados y disponibles
            - Todas las dependencias técnicas y funcionales identificadas y gestionadas
        - ***Para Inicio de Testing***
            - Build estable: Versión de desarrollo etiquetada y desplegada en ambiente de testing
            - Unit tests pasando: 100% de los tests unitarios ejecutados exitosamente
            - Documentación actualizada: Changelog y documentación técnica disponible
        
    2. ### Criterio de Salida - Definition of Done (DOD)

        - **Desarrollo**
            - Código completado: Funcionalidad implementada según criterios de aceptación
            - Code review aprobado: Revisión de pares completada y aprobada
            - Tests unitarios Implementados
        - **Calidad**
            - Casos de prueba ejecutados: 100% de los test cases definidos para la US
            - Defectos críticos/blockers: Todos resueltos y verificados
            - Pruebas cross-browser y Responsive design: Validado en dispositivos y breakpoints objetivo
        - **Product Owner**
            - Checkpoint para PO en cada User Story

6. ### Herramientas / Tecnologías / Procesos

    1. #### Stack de Testing

        - Unit Testing: Jest, React Testing Library
        - Integration / API Testing: Postman
        - E2E Testing: Playwright
        - Performance: Lighthouse CI, Web Vitals
        - Mobile Testing: BrowserStack, Playwright
        - Manejo de proyecto y TC: Jira + Xray

    2. #### Responsabilidades y Colaboración

        - **Rol del Equipo de Desarrollo**
            - Implementar y mantener tests unitarios
            - Ejecutar pruebas de integración con Postman (compartido con QA)
            - Corregir defectos identificados en menos de 24 horas (críticos) 
        - **Rol del Equipo de QA**
            - Diseñar y ejecutar la estrategia de testing por feature
            - Ejecutar pruebas de integración con Postman (compartido con Desarrollo)
            - Ejecutar pruebas exploratorias y de usabilidad
            - Mantener y expandir suite de automatización
            - Validar fixes y regresiones
        - **Colaboración Cruzada**
            - Pair testing entre desarrolladores y QA para features complejas
            - Sesiones de test review antes de cada demo de sprint
            - Compartir ownership de la calidad del producto

