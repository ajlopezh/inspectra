# Tech Stack – Inspectra (MVP v1.2)

Este documento describe las tecnologías que se usarán para el desarrollo del MVP de Inspectra.

---

## Frontend
- **HTML** – Estructura semántica de la aplicación.
- **CSS** – Estilos y diseño responsivo siguiendo Mobile First.
- **JavaScript (ES6+)** – Lógica del cliente, validaciones y manipulación de DOM.
- **React** – Librería principal para construir la interfaz y manejar componentes.

---

## Backend / Base de Datos
- **Firebase**
  - Authentication – Manejo de usuarios y roles (admin, executor).
  - Firestore – Almacenamiento de auditorías y datos estructurados.

---

## Herramientas de Desarrollo
- **Git & GitHub** – Control de versiones y repositorio remoto.
- **Visual Studio Code** – IDE principal para desarrollo.
- **Chrome / Firefox DevTools** – Depuración de frontend.

---

## Librerías / Dependencias Permitidas
- **Chart.js** – Visualización de métricas tipo Pareto en dashboard.
- **No se permiten otras librerías externas** para estilos o lógica en el MVP.

---

## Principios
- Mobile First – Priorizar diseño para dispositivos móviles.
- Minimalismo y coherencia visual – Seguir el Design System del proyecto.
- Todo el cálculo de métricas y exportación se realiza **en el frontend**.

---

## 🚫 Tecnologías / Servicios NO Permitidos
- Frameworks de UI como **Tailwind, Bootstrap, Material UI**.
- Librerías externas adicionales para la interfaz o lógica.
- Servicios pagos o de terceros fuera de Firebase.


> Nota: El MVP debe limitarse estrictamente a **HTML, CSS, JavaScript, React y Firebase** para asegurar enfoque, simplicidad y cumplimiento del alcance definido.