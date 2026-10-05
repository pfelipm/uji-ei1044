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
