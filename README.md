# Inspectra 🎐

Inspectra es una aplicación web para inspección de calidad industrial.

Su propósito es digitalizar checklists de inspección de bobinas de acero, estructurar la captura de datos desde el origen y generar métricas básicas que apoyen procesos de mejora continua.

Este repositorio contiene la versión MVP (Minimum Viable Product).

---

## 🎯 Objetivo del Proyecto

En muchos entornos industriales, las auditorías de calidad se realizan en papel o en formatos no estructurados, lo que dificulta:

- Estandarizar el registro de defectos.
- Generar análisis automáticos.
- Visualizar tendencias de calidad.
- Construir métricas confiables.

Inspectra resuelve este problema mediante:

- Captura estructurada de datos.
- Almacenamiento en base de datos.
- Cálculo automático de indicadores.
- Visualización simple de resultados.

---

## 🚀 Funcionalidades del MVP

- Autenticación de usuarios (Email + Password).
- Registro de auditorías de bobinas de acero.
- Lógica automática de conformidad.
- Dashboard con:
  - Total de auditorías.
  - Total de auditorías conformes.
  - Porcentaje de conformidad.
  - Gráfico Pareto de defectos.
- Exportación de auditorías en formato CSV.

---

## 👤 Roles de Usuario

### Administrator
- Crear auditorías.
- Visualizar todas las auditorías.
- Acceder al dashboard.
- Exportar datos.

### Executor
- Crear auditorías.
- Visualizar auditorías.
- Acceder al dashboard.
- Exportar datos.

> En el MVP no existe aislamiento de datos entre usuarios.

---

## 🛠 Tech Stack

Frontend:
- React (Functional Components + Hooks)
- JavaScript (ES6+)
- CSS puro

Backend / Base de Datos:
- Firebase Authentication
- Cloud Firestore

Visualización:
- Chart.js

Deployment:
- Firebase Hosting o Vercel

---

## 📊 Modelo de Datos (Firestore)

Colección: `audits`

Estructura del documento:

```
{
  auditDate: Timestamp,
  providerName: string,
  coilId: string,
  defect1: string,
  defect2: string | null,
  defect3: string | null,
  observations: string,
  isConform: boolean,
  createdAt: Timestamp,
  createdBy: string
}
```

---

## 🎨 Diseño

El sistema sigue una estética:

- Minimalista
- Mobile First
- Inspiración japonesa (simple, clara, zen)
- Paleta reducida
- Espaciado amplio
- Sin frameworks UI externos

---

## 📦 Instalación y Ejecución Local

1. Clonar el repositorio:

```
git clone <repository-url>
```

2. Instalar dependencias:

```
npm install
```

3. Configurar variables de entorno:

Crear archivo `.env` con las credenciales de Firebase.

4. Ejecutar el proyecto:

```
npm start
```

---

## 🔒 Reglas del MVP

- No incluye carga de imágenes.
- No incluye checklists dinámicos.
- No incluye eliminación de auditorías.
- No incluye backend adicional.
- Todos los cálculos del dashboard se realizan en el frontend.

---

## 📌 Roadmap Futuro

- v1.2 → Carga de imágenes.
- v2.0 → Aislamiento de datos por proveedor.
- v3.0 → Checklists personalizables.
- v4.0 → Asistente IA para clasificación automática.

---

## 📖 Filosofía

Inspectra no es solo un formulario digital.

Es una base para construir:

- Estandarización.
- Trazabilidad.
- Medición objetiva.
- Mejora continua en procesos industriales.

El MVP prioriza simplicidad, claridad técnica y escalabilidad futura.

---

Desarrollado como proyecto académico enfocado en arquitectura clara y buenas prácticas.