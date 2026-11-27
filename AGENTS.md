# AGENTS.md — Guías de desarrollo para Planifica

Este documento define las reglas de arquitectura, estilo de código, manejo de datos y flujo de trabajo que deben seguirse en todo momento al desarrollar **Planifica**.

## Stack tecnológico

- **React** (componentes funcionales y hooks)
- **TypeScript** (modo estricto)
- **Vite**
- **React Flow** (`@xyflow/react`)
- **CSS** puro y mantenible
- **JSON** para datos académicos
- **LocalStorage** para persistencia de progreso del usuario

## Principios de desarrollo

1. **TypeScript estricto:** Usar TypeScript en modo estricto (`"strict": true`). Evitar el uso de `any`; definir interfaces y tipos explícitos para modelos, props y estados.
2. **React moderno:** Usar exclusivamente componentes funcionales y hooks (`useState`, `useEffect`, `useMemo`, custom hooks, etc.).
3. **Componentes pequeños y enfocados:** Mantener cada componente pequeño y con una única responsabilidad clara.
4. **Separación de responsabilidades:** Separar claramente:
   - Componentes de interfaz de usuario (`components/`)
   - Modelos de dominio y tipos (`types/` o `models/`)
   - Lógica de negocio / reglas de correlatividad (`services/` o `domain/`)
   - Estado y persistencia en LocalStorage (`hooks/` / `storage/`)
   - Datos académicos (`data/`)
5. **Simplicidad:** Evitar abstracciones prematuras y dependencias innecesarias (no agregar librerías de CSS o estado global salvo necesidad justificada).
6. **Sin backend ni base de datos:** Toda la aplicación funciona del lado del cliente.
7. **Sin datos hardcodeados en la UI:** No incrustar información de planes de estudio, materias o correlatividades dentro de componentes React.
8. **Datos académicos separados de la lógica:** Los planes de estudio deben residir en archivos JSON independientes y ser consumidos mediante funciones/servicios tipados.
9. **HTML semántico y accesibilidad:** Usar etiquetas semánticas (`<main>`, `<header>`, `<nav>`, `<section>`, `<button>`, etc.) y controles accesibles (atributos `aria-*`, foco por teclado, contraste adecuado).
10. **Diseño responsivo:** La interfaz debe adaptarse correctamente a pantallas de escritorio, tablet y móviles.
11. **Integridad de los datos académicos:**
    - Nunca inventar planes de estudio reales, materias reales ni correlatividades reales de universidades.
    - Utilizar datos ficticios/de prueba claramente identificados (`mock`) hasta disponer de información académica verificada.
12. **Cambios acotados:** No reescribir ni modificar archivos no relacionados al implementar una nueva funcionalidad.
13. **Decisiones arquitectónicas:** Documentar y explicar las decisiones arquitectónicas importantes.

## Flujo de trabajo por etapa

Para cada etapa de desarrollo:
1. Explicar qué se va a cambiar y por qué.
2. Implementar la funcionalidad solicitada.
3. Ejecutar las verificaciones disponibles (`npm run build`, `npm run lint`) y corregir cualquier error.
4. Resumir qué archivos fueron creados o modificados.
5. Explicar los conceptos importantes de React y TypeScript utilizados.
6. Indicar cómo probar manualmente la implementación.
