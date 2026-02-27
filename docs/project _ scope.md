# Project Scope – Inspectra (MVP v1.2)

---

## 1. Descripción General

Inspectra es una aplicación web para inspección de calidad industrial.

Su objetivo es digitalizar checklists de inspección de bobinas de acero, estructurar la captura de datos desde el origen y generar análisis automáticos básicos que apoyen procesos de mejora continua.

El MVP está enfocado exclusivamente en inspección de bobinas de acero.

La aplicación debe desarrollarse utilizando:

- HTML
- CSS
- JavaScript
- React
- Firebase (Authentication + Firestore)

No se deben utilizar tecnologías externas adicionales ni servicios pagos.

---

## 2. Usuario Objetivo

El sistema está dirigido a:

- Supervisores de calidad.
- Inspectores industriales.
- Personal responsable de auditorías técnicas.

Usuarios que necesitan:

- Registrar defectos de manera estructurada.
- Visualizar métricas básicas de calidad.
- Exportar información para análisis externo.

---

## 3. Funcionalidades Principales (Core Features)

### 3.1 Autenticación de Usuario

- Registro e inicio de sesión mediante Email y Password.
- Autenticación implementada con Firebase Authentication.
- Cada usuario debe tener un rol asignado:
  - "admin"
  - "executor"
- El sistema debe restringir acceso a rutas protegidas si el usuario no está autenticado.

---

### 3.2 Registro de Auditorías

El usuario puede diligenciar un checklist fijo para inspección de bobinas de acero con los siguientes campos:

- Fecha de auditoría
- Nombre del proveedor
- ID de la bobina
- Defecto 1
- Defecto 2 (opcional)
- Defecto 3 (opcional)
- Observaciones

Reglas:

- defect1 es obligatorio.
- defect2 y defect3 son opcionales.
- Si defect1 = "Sin defecto":
  - defect2 y defect3 deben guardarse como null.
  - La auditoría se marca automáticamente como conforme.
- Si defect1 es diferente de "Sin defecto":
  - La auditoría se marca como no conforme.

Cada auditoría debe almacenarse como un documento independiente en la colección "audits" en Firestore.

---

### 3.3 Visualización de las auditorías realizadas en formato tabla

El usuario puede poder ver en una tabla, al estilo de excel, toda las auditorías realizadas.

Requisitos:

- La tabla debe tener títulos adecuados y las filas serán los datos registrados para todas las auditorías realizadas.
- Incluir todos los campos almacenados.

---

### 3.4 Dashboard de Métricas

El sistema debe mostrar una vista principal con:

- Total de auditorías registradas.
- Número de auditorías conformes.
- Porcentaje de conformidad.
- Gráfico tipo Pareto de defectos.

Reglas del Pareto:

- Contar defect1, defect2 y defect3.
- Excluir valores null.
- Excluir "Sin defecto".
- Ordenar de mayor a menor frecuencia.
- Visualizar usando Chart.js.

Todos los cálculos deben realizarse en el frontend (client-side).

---

### 3.5 Exportación de Datos

El usuario puede exportar todas las auditorías registradas en formato CSV.

Requisitos:

- Generación del archivo en el frontend usando JavaScript.
- Incluir todos los campos almacenados.
- Nombre del archivo:
  inspectra_audits_YYYYMMDD.csv

---

## 4. Roles de Usuario (MVP)

El sistema debe manejar dos roles:

### Administrator ("admin")

- Puede crear auditorías.
- Puede visualizar todas las auditorías.
- Puede acceder al dashboard.
- Puede exportar datos.
- No puede eliminar auditorías.

### Executor ("executor")

- Puede crear auditorías.
- Puede visualizar todas las auditorías (en el MVP).
- Puede acceder al dashboard.
- Puede exportar datos.
- No puede eliminar auditorías.

Nota:
El aislamiento de datos entre ejecutores no forma parte del MVP.

---

## 5. Modelo de Datos (Firestore)

Cada auditoría debe almacenarse en la colección:

`audits`

Estructura obligatoria del documento:

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

Reglas:

- createdAt debe generarse automáticamente al guardar.
- createdBy debe contener el UID del usuario autenticado.
- No incluir el campo role dentro del documento audit.

---

## 6. Reglas de Negocio

- El usuario debe estar autenticado para acceder al sistema.
- defect1 es obligatorio.
- defect2 y defect3 deben ser null si defect1 = "Sin defecto".
- No se permite eliminación de auditorías.
- No se permite creación dinámica de checklists en el MVP.
- Todos los cálculos del dashboard deben realizarse en el frontend.
- La aplicación debe seguir el enfoque Mobile First.

---

## 7. Exclusiones del MVP (Non-Goals)

No incluir en esta versión:

- Carga de imágenes.
- Firebase Storage.
- Checklists dinámicos.
- Gestión avanzada de usuarios desde interfaz.
- Eliminación de registros.
- Aislamiento de datos por proveedor.
- Inteligencia Artificial.
- Backend adicional distinto a Firebase.

---

## 8. Roadmap Futuro (Referencia)

v1.2 → Carga de imágenes.  
v2.0 → Aislamiento de datos por proveedor.  
v3.0 → Checklists personalizables.  
v4.0 → Asistente IA para clasificación automática.

---

## 9. Filosofía del Producto

Inspectra no es solo un formulario digital.

Es un sistema orientado a:

- Captura estructurada de datos.
- Estandarización.
- Trazabilidad.
- Medición objetiva.
- Soporte a la mejora continua.

El MVP prioriza simplicidad, claridad técnica y base sólida para escalabilidad futura.
