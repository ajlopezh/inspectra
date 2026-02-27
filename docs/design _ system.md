# Design System – Inspectra (MVP v1.0)

---

## 1. Design Philosophy

Inspectra adopta una estética japonesa minimalista.

Principios fundamentales:

- Simplicidad visual.
- Jerarquía clara.
- Colores limitados.
- Interfaz silenciosa y ordenada.
- Sensación de calma y precisión.

La experiencia debe transmitir:

- Facilidad de uso.
- Claridad mental.
- Control sin saturación visual.

---

## 2. Design Approach

### Mobile First (Obligatorio)

El diseño debe construirse primero para pantallas móviles.

Base width de referencia:
- 375px

Breakpoints:

- Mobile: 0px – 767px (base)
- Tablet: 768px+
- Desktop: 1024px+

Reglas:

- Layout vertical por defecto.
- Botones full-width en móvil.
- Cards apiladas verticalmente.
- Márgenes amplios.
- Navegación superior simple (sin sidebar en MVP).

---

## 3. Color Palette

La paleta debe ser limitada y equilibrada.

### Primario (Acción)
- #1F3A5F (Azul profundo japonés)
Usar en:
- Botones principales
- Enlaces activos
- Elementos destacados

### Secundario (Éxito)
- #4C7A57 (Verde suave)
Usar en:
- Mensajes de confirmación
- Indicadores positivos

### Fondo General
- #FAFAF7 (Blanco cálido)
Evita el blanco puro para reducir fatiga visual.

### Superficie (Cards)
- #FFFFFF

### Texto Principal
- #2E2E2E (Gris oscuro suave)

### Texto Secundario
- #6B6B6B (Gris medio)

### Error
- #B23A3A (Rojo tenue)

Regla:
No utilizar colores adicionales fuera de esta paleta en el MVP.

---

## 4. Typography

### Fuente Principal
- 'Inter', sans-serif

Fallback:
- system-ui, sans-serif

### Jerarquía

H1:
- 28px (mobile)
- 32px (desktop)
- font-weight: 600

H2:
- 20px
- font-weight: 600

Texto cuerpo:
- 16px
- font-weight: 400
- line-height: 1.6

Texto pequeño:
- 14px

Reglas:

- No usar más de 2 pesos tipográficos.
- Mantener alto contraste con el fondo.
- Evitar texto excesivamente pequeño.

---

## 5. Spacing System

Base unit: 8px

Escala permitida:

- 4px
- 8px
- 16px
- 24px
- 32px
- 48px

Reglas:

- Utilizar múltiplos de 8px para márgenes y padding.
- Priorizar más espacio en lugar de compactación.
- El espacio en blanco es parte esencial del diseño.

---

## 6. Border Radius & Shadows

Border-radius:

- Inputs: 8px
- Botones: 10px
- Cards: 12px

Sombras:

Cards:
box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);

Hover ligero:
box-shadow: 0 6px 16px rgba(0, 0, 0, 0.06);

Regla:
Sombras siempre sutiles. No usar sombras fuertes ni dramáticas.

---

## 7. UI Components

### 7.1 Buttons

Primary Button:

- Background: #1F3A5F
- Color texto: #FFFFFF
- Border-radius: 10px
- Padding: 12px 16px
- Width: 100% en mobile
- Transition: 0.2s ease

Hover:
- Oscurecer ligeramente el fondo.

Secondary Button:

- Fondo transparente
- Border: 1px solid #1F3A5F
- Texto: #1F3A5F

Disabled:

- Opacidad reducida
- Cursor not-allowed

---

### 7.2 Inputs / Select / Textarea

- Fondo: #FFFFFF
- Border: 1px solid #E5E5E5
- Border-radius: 8px
- Padding: 12px
- Font-size: 16px

Focus:

- Border-color: #1F3A5F
- Eliminar outline azul por defecto
- Aplicar sombra muy sutil

Errores:

- Border-color: #B23A3A
- Mostrar mensaje de error debajo del campo

---

### 7.3 Cards

- Fondo: #FFFFFF
- Border-radius: 12px
- Padding: 24px
- Sombra ligera
- Separación vertical mínima: 24px

Las cards deben organizar el contenido en bloques claros.

---

### 7.4 Navbar

- Fondo: #FFFFFF
- Border-bottom: 1px solid #E5E5E5
- Altura cómoda (mínimo 60px)
- Título alineado a la izquierda
- Información del usuario alineada a la derecha
- Sin sidebar en el MVP

---

### 7.5 KPI Cards (Dashboard)

- Número principal grande (28px o mayor)
- Label descriptivo pequeño
- Diseño centrado
- Mucho espacio interno
- Fondo blanco

---

### 7.6 Chart Container

- Usar Card como contenedor
- Padding generoso
- Gráfico con colores suaves
- Sin fondos oscuros

---

## 8. Interaction Principles

- Una acción principal por pantalla.
- Transiciones suaves (150ms–200ms).
- No usar animaciones llamativas.
- Evitar saturación visual.
- Priorizar claridad sobre decoración.

---

## 9. Accessibility Guidelines

- Mantener contraste suficiente entre texto y fondo.
- Tamaño mínimo de texto: 14px.
- Inputs y botones deben ser fácilmente clicables en móvil.
- Estados hover y focus deben ser visibles.

---

## 10. Design Constraints (MVP)

- No implementar dark mode en esta versión.
- No usar frameworks de UI externos (Material UI, Bootstrap, etc.).
- No agregar estilos fuera de este sistema.
- Mantener coherencia visual en toda la aplicación.

---

Inspectra debe sentirse ligero, ordenado y preciso.
