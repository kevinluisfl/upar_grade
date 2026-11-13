# 📋 UparGrade Studio — Hojas de Respuesta ICFES y Escáner OMR

**UparGrade Studio** es una aplicación web interactiva inspirada en herramientas como *ZipGrade*, diseñada para que los docentes puedan crear evaluaciones, generar hojas de respuestas ópticas tipo **ICFES** listas para imprimir y calificar exámenes de forma automatizada mediante un **Escáner OMR (Reconocimiento Óptico de Marcas)** usando la cámara o subiendo fotografías.

---

## ✨ Características Principales

### 1. Creador de Exámenes y Clave de Respuestas (Answer Key)
- **Configuración Flexible:** Define el título de la evaluación, grado/asignatura y cantidad de preguntas (`10`, `15`, `20`, `25`, `30`, `40` o `50`).
- **Opciones por Pregunta:** Soporta preguntas de **3 opciones (`A, B, C`)**, **4 opciones (`A, B, C, D`)** o **5 opciones (`A, B, C, D, E`)**.
- **Escala de Calificación Personalizable:** Configura la **Nota Máxima** (ej. `5.0`, `10.0`, `100`) y la **Nota Mínima** (ej. `1.0` o `0.0`). El sistema calcula en tiempo real cuánto vale cada acierto y cuál es la nota aprobatoria (60%).
- **Matriz Interactiva de Clave:** Marca la burbuja correcta de cada pregunta con un clic, genera claves aleatorias de prueba o usa el **Pegado Rápido** escribiendo directamente la secuencia de letras (ej. `ABCDABCDAA...`)[cite: 26].
- **Gestión Local y Respaldo JSON:** Guarda múltiples exámenes en el navegador (`localStorage`) y exporta o importa copias de seguridad en `.json` (permitiendo elegir entre **sumar a los actuales** o **sobrescribir todo**).

### 2. Generador de Hojas de Respuesta Tipo ICFES (Imprimibles y PNG)
- **Marcas Fiduciales OMR:** Cada hoja incluye 4 marcadores negros de esquina en coordenadas geométricas exactas para el encuadre del escáner óptico.
- **Dos Estilos de Diseño:**
  1. **Formato Completo ICFES:** Incluye encabezado institucional, cajas para nombre, fecha y nota, instrucciones de llenado y columnas de burbujas.
  2. **Formato Simplificado (Solo Esencial):** Diseño ultracompacto que elimina los textos largos para maximizar el ahorro de papel en el aula.
- **Impresión Múltiple (Hasta 6 por Página):** Configura **1, 2, 4 o 6 hojas de respuesta por página imprimible**.
- **Orientación Inteligente:** Selector de orientación **Automática** (ajusta entre vertical y horizontal según la cantidad de preguntas y copias), **Vertical (Portrait)** u **Horizontal (Landscape)**.
- **Hoja Guía del Docente:** Opción para sombrear automáticamente las respuestas correctas en la vista previa, impresión o descarga directa en **Imagen PNG**.

### 3. Escáner Óptico OMR Automatizado
- **Tres Métodos de Escaneo:**
  1. **Cámara en Vivo:** Activa la cámara del dispositivo móvil o computador con guías de encuadre para capturar la hoja.
  2. **Subida de Imagen:** Carga una fotografía o captura de la hoja de respuestas.
  3. **Simulador Integrado:** Genera una hoja rellenada de prueba con un clic para verificar el funcionamiento del lector óptico.
- **Control de Sensibilidad de Tinta/Lápiz:** Deslizador en tiempo real (`18%` a `65%`) para ajustar el umbral de detección de oscuridad según la iluminación de la foto o la intensidad del lápiz.
- **Auditoría Visual y Corrección en 1 Clic:**
  - Dibuja anillos **verdes** sobre los aciertos, **rojos** sobre los errores y **azules/ámbar** indicando cuál era la respuesta correcta o si hubo preguntas en blanco/doble marca.
  - Incluye un panel lateral de revisión rápida donde el docente puede ajustar manualmente cualquier respuesta detectada con un solo clic y recalcular la nota al instante.

### 4. Planilla de Calificaciones y Estadísticas (Gradebook)
- **Indicadores del Grupo (KPIs):** Calcula automáticamente el total de estudiantes evaluados, el **Promedio del Grupo**, el **Porcentaje de Aprobados (≥ 60%)** y la **Mejor Nota**[cite: 25].
- **Filtros y Búsqueda:** Filtra calificaciones por evaluación o busca estudiantes por nombre o código[cite: 25].
- **Exportación a Excel (`.csv`) con Separador Configurable:** Descarga la planilla completa con soporte UTF-8 y selector de delimitador (**Punto y coma `;`** por defecto para Excel en español, **Coma `,`**, **Tabulación** o **Barra `|`**)[cite: 25].

### 5. Interfaz y Personalización
- **Diseño Indigo Studio:** Estética limpia y uniforme con soporte nativo para **Tema Claro / Oscuro** y traducción completa **Español / Inglés (`ES` / `EN`)**.

---

## 🚀 Instalación y Uso

La aplicación funciona **100% en el navegador del cliente** (sin servidores ni instalación de dependencias externas):

1. Clona este repositorio o descarga los archivos del proyecto:
   ```bash
   git clone [https://github.com/kevinluisfl/upargrade-studio.git](https://github.com/kevinluisfl/upargrade-studio.git)