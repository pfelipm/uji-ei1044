# Guía y convenciones del proyecto EI1044

## 1. Estilo y maquetación de SPAs (HTML / Tailwind CSS)

### Listas y viñetas (sangría francesa)
* **Nunca usar `list-inside`** en listas desordenadas (`<ul>`) u ordenadas (`<ol>`) que contengan texto explicativo o párrafos que puedan saltar a una segunda línea, ya que coloca el marcador dentro del flujo de texto e impide la sangría francesa (las líneas secundarias quedan debajo de la viñeta).
* **Usar siempre posición exterior con padding**: aplicar `list-disc list-outside pl-5` (o `list-decimal list-outside pl-5`) junto a `space-y-...`. De este modo:
  - El marcador (viñeta o número) se posiciona a la izquierda en el área de padding.
  - El texto de las líneas subsiguientes se alinea verticalmente por la izquierda con la primera línea (sangría francesa).

## 2. Tipografía y redacción en español

### Capitalización (Sentence case)
* Seguir las normas ortográficas de la RAE: en títulos, subtítulos, encabezados (`<h2>`, `<h3>`), etiquetas y descripciones de tarjetas, usar mayúscula únicamente en la letra inicial de la frase y en nombres propios o términos técnicos específicos (p. ej., *PowerShell*, *Azure Cloud Shell*).
* Evitar la capitalización de estilo anglosajón (*Title Case*) que capitaliza cada palabra.

## 3. Diseño pedagógico y triple función de las SPAs

Todas las SPAs del proyecto deben diseñarse para cumplir simultáneamente **tres funciones**:

1. **Dirigir la secuencia didáctica en el aula:**
   - Estructurar cada SPA en **fases o pestañas secuenciales** (navegables también con botones *Anterior / Siguiente* o teclado) que guíen de forma natural el ritmo de la sesión sin obligar al docente a consultar constantemente el documento del plan de clases.
   - Incluir al final de la última fase/pestaña un **botón de transición directa** hacia la siguiente SPA de la secuencia didáctica.

2. **Apoyar la explicación y las dinámicas participativas (sin «spoilers»):**
   - Nunca mostrar en pantalla notas internas para el profesor ni destripar de entrada las conclusiones de un debate o pregunta.
   - Para dinámicas y debates, presentar la **pregunta o reto en formato grande y limpio** para abrir el turno de palabra, ocultando la síntesis o dictamen técnico tras un botón discreto (`💡 Mostrar claves y conclusión técnica`).
   - Integrar simuladores, clasificadores y laboratorios interactivos que permitan experimentar conceptos en directo sobre casos realistas (p. ej., *Keraben Grupo* o incidentes reales de la *UJI*).

3. **Servir como material de estudio y consulta autónoma en casa (lectura a dos niveles):**
   - Dado que los apuntes en PDF heredados son estáticos o están desactualizados, las SPAs deben ofrecer **despliegue de información a dos niveles**:
     - **Nivel 1 (proyección en aula):** visual, directo, con titulares claros, métricas clave y baja densidad de texto inicial.
     - **Nivel 2 (estudio en casa):** bloques desplegables (`🔎 Desplegar análisis técnico completo`) y paneles de síntesis revelables con el rigor técnico, normativo y práctico actualizado que el estudiantado necesita para repasar por su cuenta.

### Reglas técnicas adicionales (Tailwind CDN y compatibilidad dual Google Sites / GitHub Pages)
* **Barras superiores de pestañas/fases limpias en una sola línea:** Mantener etiquetas concisas en los botones de pestañas superiores (`flex flex-wrap justify-center gap-2 sm:gap-3`) sin añadir botones redundantes `◀ Anterior / Siguiente ▶` en esa misma barra (la navegación secuencial por teclado se habilita escuchando `ArrowLeft` y `ArrowRight`).
* **Botones de pestañas/fases activos:** Al definir clases activas para botones de navegación o filtro (`.tab-btn.active`, `.filter-chip.active`), incluir siempre la pseudoclase `:hover` y `!important` en `background-color` y `color` (`.tab-btn.active, .tab-btn.active:hover { background-color: #0f172a !important; color: #ffffff !important; }`) para evitar que las utilidades `hover:text-...` o `hover:bg-...` inyectadas dinámicamente por el CDN de Tailwind sobrescriban el contraste al pasar el ratón.
* **Ocultación automática de enlaces entre SPAs dentro de Google Sites (`.hide-in-embed`) y centrado exacto del botón central:** Incluir siempre en el `<head>` el detector de iframe (`if (window.self !== window.top) document.documentElement.classList.add('is-embedded');`) y la regla `.is-embedded .hide-in-embed { display: none !important; }`. Maquetar la barra de navegación secuencial inferior entre módulos (`← Anterior | 📋 Volver al índice general | Siguiente →`) con `grid grid-cols-1 sm:grid-cols-3 items-center gap-4 hide-in-embed`, aplicando `justify-self-center sm:justify-self-start` al botón izquierdo, `justify-self-center` al botón central y `justify-self-center sm:justify-self-end` al derecho, para que el botón central quede siempre matemáticamente centrado con independencia de la longitud de los textos laterales.
* **Sincronización de copias locales:** Siempre que se cree o edite una SPA de los Temas 4 o 5 en el repositorio (`ei1044/t4/` o `ei1044/t5/`), actualizar simultáneamente su copia espejo en la carpeta de materiales de la asignatura (`T4 Seguridad de la información/SPA/` o `T5 Metodologías gestión Servicios Informaticos/SPA/`).

## 4. Hoja de ruta y recordatorios pendientes

* **Extender navegación `.hide-in-embed` al Tema 5:** Aplicar el mismo bloque de navegación secuencial inferior (`← Anterior | 📋 Volver al índice general | Siguiente →`) con detección de iframe a todas las SPAs de `t5/` cuando se aborde su revisión.
* **Homogeneizar navegación en Temas 1, 2 y 3 (`t1/`, `t2/`, `t3/`):** Recordar al usuario, una vez cerrados los Temas 4 y 5, la tarea pendiente de incorporar y unificar este mismo mecanismo de navegación secuencial `.hide-in-embed` en las SPAs de los Temas 1 y 3 (y homogeneizar su estilo con el Tema 2) para que todo el repositorio sea 100 % uniforme.
