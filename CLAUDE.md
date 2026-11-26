# Instrucciones para Claude Code

Este proyecto es una web estática de un solo archivo (`index.html`) que se publica con GitHub Pages desde la rama `main`, carpeta raíz.

Tarea de publicación:
1. Comprueba que `git` y `gh` están instalados y que `gh auth status` muestra una sesión iniciada. Si no hay sesión, pide al usuario que ejecute `gh auth login` él mismo.
2. Inicializa el repositorio con la rama `main`, haz el commit inicial con todos los archivos.
3. Crea un repositorio PÚBLICO en la cuenta del usuario llamado `taller-de-cubos` y sube el código (`gh repo create taller-de-cubos --public --source=. --push`). Confirma el nombre con el usuario antes de crearlo.
4. Activa GitHub Pages desde `main` y la raíz:
   `gh api -X POST repos/{owner}/taller-de-cubos/pages -f "source[branch]=main" -f "source[path]=/"`
5. Espera a que el despliegue termine (`gh api repos/{owner}/taller-de-cubos/pages` hasta que `status` sea `built`) y da al usuario la dirección final, del tipo `https://<usuario>.github.io/taller-de-cubos/`.

Para cambios futuros: edita `index.html`, haz commit y push a `main`; GitHub Pages se actualiza solo en uno o dos minutos.
