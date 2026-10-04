# Administración de Sistemas Informáticos (EI1044) - UJI

Materiales docentes interactivos para la asignatura optativa de 4º curso **Administración de Sistemas Informáticos (EI1044)** del Grado en Ingeniería Informática de la **Universitat Jaume I**.

> 📅 **Curso Académico:** 2026/2027 (Materiales revisados y actualizados).  
> 🌐 **Portal Web en GitHub Pages:** [https://pfelipm.github.io/uji-ei1044/](https://pfelipm.github.io/uji-ei1044/)  
> 🤖 **Tutor Inteligente de la Asignatura:** [Gema de IA: PowerShell Master](https://gemini.google.com/gem/11OPVdGPKX0oEXI1_DsuOK9OU_xTC0EYO?usp=drive_link)

---

## 📚 Estructura del repositorio

Este repositorio aloja las Single Page Applications (SPAs) interactivas desarrolladas para las sesiones de teoría y aula de informática de la asignatura. A lo largo del curso se irán incorporando los materiales de los diferentes temas:

* **`t2/` · Tema 2: Introducción a la Automatización Moderna con PowerShell 7 (Sesión de 2 horas)**
*(Próximamente se incorporarán las SPAs correspondientes al resto de temas de la asignatura).*

---

## 🎯 Tema 2: Introducción a PowerShell 7

Conjunto de **10 infografías interactivas (SPAs)** autocontenidas desarrolladas con **Tailwind CSS**, optimizadas para proyectarse en el aula y para integrarse en el Aula Virtual mediante **Google Sites**:

| # | Módulo | Fichero | Conceptos clave | Enlace directo |
| :-: | :--- | :--- | :--- | :--- |
| **01** | **La navaja suiza del sysadmin** | `La navaja suiza del sysadmin.html` | Automatización a escala, terminales (Cloud Shell, VS Code), Bash vs. pwsh (texto vs. objetos). | [Ver Módulo 01](https://pfelipm.github.io/uji-ei1044/t2/La%20navaja%20suiza%20del%20sysadmin.html) |
| **02** | **Un análisis de PowerShell 7** | `Un análisis de PowerShell 7.html` | Comparativa interactiva PS 5.1 vs. 7, operadores modernos (`? :`, `??`, `&&`, `\|\|`), `.NET 8+`, multiplataforma. | [Ver Módulo 02](https://pfelipm.github.io/uji-ei1044/t2/Un%20an%C3%A1lisis%20de%20PowerShell%207.html) |
| **03** | **El universo de los objetos** | `El universo de los objetos.html` | Propiedades, métodos, descubrimiento con `Get-Member` (`gm`), tubería (`\|`) con `Where-Object`, `Sort-Object` y `Select-Object`. | [Ver Módulo 03](https://pfelipm.github.io/uji-ei1044/t2/El%20universo%20de%20los%20objetos.html) |
| **04** | **Encadenamiento de comandos** | `Encadenamiento.html` | Tubería de datos (`\|`) vs. flujo de control (`&&`, `\|\|`), estado con `$?` frente a objeto en pipeline `$_`. | [Ver Módulo 04](https://pfelipm.github.io/uji-ei1044/t2/Encadenamiento.html) |
| **05** | **Variables y operadores** | `Variables y operadores.html` | Tipado dinámico y estricto, comillas simples vs. dobles con `$($obj.Prop)`, operadores con guion y **la regla del `$null` a la izquierda**. | [Ver Módulo 05](https://pfelipm.github.io/uji-ei1044/t2/Variables%20y%20operadores.html) |
| **06** | **Colecciones de datos** | `Colecciones de datos.html` | Arrays (listas indexadas en 0, adición, rango `1..n`) y Hashtables (`@{}` diccionarios clave-valor). Criterios de diseño. | [Ver Módulo 06](https://pfelipm.github.io/uji-ei1044/t2/Colecciones%20de%20datos.html) |
| **07** | **Controlando el flujo** | `Controlando el flujo.html` | Condicionales `if/elseif/else` y `switch`. Bucles `foreach` (idiomático sobre colecciones), `for`, `while` y `do-while`. | [Ver Módulo 07](https://pfelipm.github.io/uji-ei1044/t2/Controlando%20el%20flujo.html) |
| **08** | **Funciones y scripts** | `Funciones y scripts.html` | Funciones en memoria vs. scripts `.ps1`, bloque `param()`, `[CmdletBinding()]`, dot-sourcing y **seguridad (`ExecutionPolicy`)**. | [Ver Módulo 08](https://pfelipm.github.io/uji-ei1044/t2/Funciones%20y%20scripts.html) |
| **09** | **Gestión de errores** | `Gestión de errores.html` | Errores *Non-Terminating* vs. *Terminating*, bloques `try/catch/finally`, `-ErrorAction Stop` e inspección con `$_.Exception`. | [Ver Módulo 09](https://pfelipm.github.io/uji-ei1044/t2/Gesti%C3%B3n%20de%20errores.html) |
| **10** | **Interactuando con el exterior** | `Módulos y ficheros.html` | PowerShell Gallery (`Install-Module`), ficheros planos, JSON (`ConvertFrom-Json`) y transformación mágica de CSV a objetos. | [Ver Módulo 10](https://pfelipm.github.io/uji-ei1044/t2/M%C3%B3dulos%20y%20ficheros.html) |

---

## ✨ Características de las SPA

* **📋 Botón «Copiar código»:** Todos los bloques de código incorporan un botón en la esquina superior derecha para copiar el snippet con un solo clic y pegarlo directamente en PowerShell o VS Code.
* **🔄 Navegación adaptable y contextual:**
  * **En GitHub Pages:** Muestra la barra de navegación secuencial en el pie (`← Módulo anterior` y `Módulo siguiente →`) y el botón al `Índice` para facilitar la navegación autónoma.
  * **En Google Sites (Iframe):** Detecta automáticamente la incrustación y **oculta estos enlaces** para ofrecer una experiencia limpia e integrada con el menú del Site.
* **🤖 Integración con IA generativa:** Acceso directo en el pie de cada módulo a la gema personalizada **PowerShell Master**, diseñada para asistir a los alumnos en la modernización de scripts clásicos hacia PowerShell 7.
* **🎓 Píldoras técnicas avanzadas para 4.º de carrera:**
  * **La trampa del `$null`:** Por qué en PowerShell siempre se escribe `$null -eq $var` en lugar de `$var -eq $null`.
  * **Comillas simples vs. dobles y subexpresiones `$($obj.Prop)`:** Manipulación precisa de strings sin romper propiedades.
  * **Directivas de ejecución (`ExecutionPolicy`):** Políticas `RemoteSigned` vs `Bypass`, ámbito `-Scope CurrentUser` y su rol como cinturón de seguridad.

---

## 🚀 Publicación e integración en Google Sites

Al estar publicado en **GitHub Pages**, no es necesario copiar y pegar bloques de código HTML dentro del editor de Google Sites:

1. En tu Google Site, añade una página o sección.
2. Selecciona **Insertar > Por URL**.
3. Pega la URL directa del módulo correspondiente (por ejemplo: `https://pfelipm.github.io/uji-ei1044/t2/La%20navaja%20suiza%20del%20sysadmin.html`) y elige la opción **Página completa**.
4. **Ventaja:** Cualquier actualización que realices en el repositorio Git se reflejará **automáticamente en Google Sites** tras hacer `git push`.

---

## 👤 Autoría

* **Pablo Felip Monferrer**  
  Profesor Asociado  
  [Departamento de Lenguajes y Sistemas Informáticos (LSI)](https://www.uji.es)  
  **Universitat Jaume I (UJI)**  
  🌐 Sitio web personal / docente: [https://www.pablofelip.uji.es](https://www.pablofelip.uji.es)

---

## 📄 Licencia

Este repositorio y todos sus materiales formativos se distribuyen bajo la licencia:

**[Creative Commons Atribución-NoComercial-CompartirIgual 4.0 Internacional (CC BY-NC-SA 4.0)](LICENSE)**

Usted es libre de:
* **Compartir:** Copiar y redistribuir el material en cualquier medio o formato.
* **Adaptar:** Remezclar, transformar y crear a partir del material.

Bajo las siguientes condiciones:
* **Atribución:** Debe dar crédito a la autoría de manera adecuada, brindar un enlace a la licencia e indicar si se han realizado cambios.
* **No comercial:** No puede hacer uso del material con propósitos comerciales.
* **Compartir igual:** Si remezcla, transforma o crea a partir del material, deberá difundir sus contribuciones bajo la misma licencia que el original.

Para más detalles, consulte el archivo [LICENSE](LICENSE) o visite [https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es).
