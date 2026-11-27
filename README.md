# Planifica

**Planifica** es una aplicación web interactiva para explorar planes de estudio universitarios, visualizar materias y analizar sus correlatividades (prerrequisitos) de forma clara e intuitiva.

## Propósito

Facilitar a estudiantes la comprensión visual de su carrera universitaria:
- Explorar el grafo de materias y sus dependencias (correlatividades).
- Consultar información detallada de cada asignatura.
- Llevar un registro personal del progreso académico guardado localmente en el navegador.

## Tecnologías principales

- **React 19** — Biblioteca de interfaz de usuario basada en componentes funcionales y hooks.
- **TypeScript** — Tipado estático estricto para mayor seguridad y mantenibilidad.
- **Vite** — Herramienta de desarrollo rápida y empaquetador moderno.
- **React Flow (`@xyflow/react`)** — Visualización interactiva de grafos y mapas de correlatividades *(por instalar en la etapa correspondiente)*.
- **CSS** — Hojas de estilo nativas y mantenibles, sin dependencias innecesarias.
- **JSON** — Archivos locales estructurados para los datos académicos.
- **LocalStorage** — Persistencia local del progreso del usuario en el navegador (sin backend ni base de datos).

## Comandos de desarrollo

> **Nota en Windows PowerShell:** Si la ejecución de scripts `.ps1` está restringida en tu sistema, utiliza `npm.cmd` en lugar de `npm`.

- **Instalar dependencias:**
  ```bash
  npm install
  ```
- **Iniciar servidor de desarrollo (con recarga en caliente / HMR):**
  ```bash
  npm run dev
  ```
- **Verificar tipos y compilar para producción:**
  ```bash
  npm run build
  ```
- **Ejecutar el linter (ESLint):**
  ```bash
  npm run lint
  ```
- **Previsualizar la compilación de producción:**
  ```bash
  npm run preview
  ```
