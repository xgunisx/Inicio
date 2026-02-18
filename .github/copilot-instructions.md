# Copilot / AI agent instructions

Propósito: ayudar a agentes de IA a ser productivos rápidamente en este workspace pequeño, multi-proyecto y estático.

Contexto general
- Estructura principal: proyectos estáticos y ejemplos pequeños:
  - `CSS 1/` — HTML + `style.css` (página estática). Ejemplo principal: `CSS 1/index.html`.
  - `Design 1/` — imágenes y diseño (ej.: `yoyoyoy.jfif`).
  - `Python/` — script de ejemplo: `Hola_mundo.py`.
  - `VS prueba 1/` — otro ejemplo HTML con carpeta `Img/`.

Big picture / por qué así
- No existe un build system ni dependencias externas: la mayoría de los archivos son HTML/CSS estáticos y unos pocos scripts Python de ejemplo.
- Los cambios típicos son edición de HTML, CSS o reemplazo/optimización de imágenes. Mantener rutas relativas y cuidado con nombres de carpeta que contienen espacios (p.ej. `Visual Studio Carpet`).

Flujos de trabajo críticos (qué hace falta saber)
- Previsualizar páginas: abrir `index.html` en un navegador o usar la extensión Live Server de VS Code.
  - Ejemplo (terminal PowerShell desde la carpeta del proyecto):
    ```powershell
    # Abrir un archivo HTML con el navegador por defecto (Windows)
    start "" "CSS 1\index.html"
    ```
- Ejecutar el script Python de ejemplo:
  ```powershell
  python "Python\Hola_mundo.py"
  ```
- No hay `npm`, `pip` o CI configurados por defecto. Si creas toolchain, documenta comandos en este archivo.

Convenciones y patrones específicos del repo
- Rutas relativas: las páginas referencian activos usando rutas relativas locales. Al mover archivos, actualiza `src`/`href` en los HTML.
- Nombres de carpetas con espacios: evita romper rutas en scripts; usa siempre comillas cuando ejecutes rutas con espacios.
- Archivos de ejemplo: `CSS 1/index.html` y `VS prueba 1/index.html` muestran la estructura esperada de assets.

Integraciones externas y puntos de contacto
- Actualmente no hay APIs ni servicios externos. Las imágenes y recursos son locales (`Design 1/`, `VS prueba 1/Img/`).

Tareas comunes y ejemplos concretos
- Cambiar estilos globales: editar `CSS 1/style.css` y recargar `CSS 1/index.html`.
- Reemplazar imagen: si añades `Design 1/nueva.jpg`, actualiza la referencia en el HTML correspondiente.
- Añadir una página: crear `nueva_carpeta/index.html` y enlazar desde el menú existente con ruta relativa.

Cómo fusionar si ya existe `.github/copilot-instructions.md`
- Si el archivo ya existe, conserva cualquier sección con contexto de proyecto local (ej.: comandos personalizados) y añade/actualiza las secciones "Flujos de trabajo críticos" y "Convenciones".

Notas para el agente
- Sé explícito en los cambios: cuando modifiques un `index.html`, indica la ruta exacta y la línea aproximada del cambio.
- Prioriza no romper rutas relativas ni eliminar activos sin actualizar las referencias.
- Si propones añadir herramientas (p.ej. `npm` o `venv`), documenta comandos de instalación y por qué son necesarios.

Preguntas útiles para el humano
- ¿Quieres un build/test pipeline? ¿Deseas que agregue un README principal con instrucciones de uso?

Última revisión: generar o actualizar según feedback.

puedo poner un link en unu boton?
Sí, puedes poner un enlace en un botón utilizando HTML. Aquí tienes un ejemplo de cómo hacerlo:

```html<button onclick="window.location.href='https://www.ejemplo.com';">Ir a Ejemplo</button>
```y con un numero de telefono

Sí, también puedes poner un enlace a un número de teléfono en un botón utilizando el esquema `tel:`. Aquí tienes un ejemplo:

```html<button onclick="window.location.href='tel:+1234567890';">Llamar al +1234567890</button>
```y con instgramSí, puedes poner un enlace a un perfil de Instagram en un botón utilizando HTML. Aquí tienes un ejemplo:
```html<button onclick="window.location.href='https://www.instagram.com/tu_usuario/';">Visitar
que va en form action?¿y en method?En un formulario HTML, el atributo `action` especifica la URL a la que se enviarán