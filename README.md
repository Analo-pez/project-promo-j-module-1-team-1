**The A Team**

The A-Team nace de nuestras ganas de aprender a programar. Nos
identificamos con el comando de la famosa serie de los ochenta, no
solo porque nuestras iniciales coinciden, sino también por la
capacidad organizativa de sus miembros y su determinación para
enfrentarse a problemas y sobrevivir a circunstancias difíciles.

El modus operandi del A-Team consistía en recopilar información,
investigando cada caso hasta disponer del material necesario para
elaborar un plan capaz de confrontar "a los malos" y esquivar
milagrosamente las detenciones de la policía. Entre persecución y
explosión, como equipo, Hannibal, Murdock, Fénix, M.A y Amy, echaban
mano de la capacidad de estrategia, el sacrificio, las habilidades
técnicas y la inteligencia, nosotras ademas tenemos en nuestro poder
el código.

![EquipoA](http://beta.adalab.es/project-promo-j-module-1-team-1/)

# The A-Team

Bienvenidas al Readme del Proyecto **Equipo-A** donde os compartimos los secretos de nuestro código y os damos algunas pautas para profundizar en nuestro trabajo.

Este proyecto forma parte del primer módulo del curso de programación para mujeres de Adalab, durante el que desarrollamos **nuestra primera página web!**

## ¿Qué es The A- Team Project?

Una web para dar a conocer nuestros perfiles profesionales y facilitar el contacto con posibles empresas interesadas.

The A-Team Project nos permite compartir nuestra historia como adalabers y demostrar algunas de las capacidades adquiridas durante el curso tanto a nivel técnico como organizativo (gestión de trabajo en grupo, metodología agile, trabajo en remoto).

Además de atender a un diseño responsive y a una estructura de maquetación muy diversa la web incorpora un formulario de contacto, animaciones y enlaces a diferentes secciones dentro de la página.

## Composición de nuestra página

Esta página incluye un motor de plantillas HTML, el preprocesador SASS y un servidor local además de 3 tipos de ficheros y carpetas:

- Los ficheros que están sueltos en la raíz del repositorio, como gulpfile.js, package.json... Son la configuración del proyecto y no necesitamos modificarlos.
- La carpeta `src/`: son los ficheros de nuestra página web, como HTML, CSS, JS...
- Las carpetas `public/` y `docs/`, que son generadas automáticamente cuando arrancamos el proyecto. El Kit lee los ficheros que hay dentro de `src/`, los procesa y los genera dentro de `public/` y `docs/`.

La estructura de nuestra página web responde a las siguientes secciones:

- Un`index.html/`
- Un `forms.html/` que recoge el formulario de contacto vinculado al index principal.
- Un Footer`footer/`.
- Un Header`header/`.
- `CardAdalaber/`. Que incorpora las tarjetas personalizables de cada una de nosotras.
- `Adalabers/`.
- `Team/`.

## Funcionalidad.

La web cuenta con un diseño responsive adaptado a todo tipo de dispositivos y estructurado a partir de una cabecera fija con botones que linkean a diferentes secciones de la página. El contenido se estructura en una sección de información sobre nuestro proyecto, las fortalezas y debilidades del equipo y una descripción personalizada de cada una de nosotras seguido por un footer linkeado al comienzo de la página.  

El proyecto incorpora además un formulario de contacto e incluye animaciones y transiciones para hacer la página más visual y coherente para los y las usuarias. 

## Construido con

- HTML, SASS.
- Gulp,
- Starter Kit Adalab.
- Node JS y NPM
- VS Code

## Autoras

- Alexandra "Murdock" López.
- Ana "Hannibal" López.
- Alba "Fénix" San Martín.
- Amanda "M.A." Palma.
- Ana "Amy" Fernández.

## Mantenimiento.

Este es un proyecto abierto con lo que invitamos a cualquier colaboradora a clonarse nuestro repositorio y añadir mejoras y sugerencias.

## Guía de inicio rápido para trabajar sobre la base de nuestro proyecto.

Este es un proyecto abierto, considéralo tuyo y en caso de querer trabajar sobre nuestros pasos sigue las siguientes indicaciones.

> **NOTA:** Necesitas tener instalado [Node JS](https://nodejs.org/) para trabajar con este Proyecto:

1. **Crea tu propio repositorio.**
1. Clona **nuestro proyecto**.
   - Si has decidido clonar este repo, no debes copiar la carpeta `.git`. Si lo haces estarás machacando tu propio repositorio.
1. **Abre una terminal** en la carpeta raíz de tu repositorio.
1. **Instala las dependencias** locales ejecutando en la terminal el comando:

```bash
npm install
```

### Pasos para arrancar el proyecto:

Una vez hemos instalado las dependencias, vamos a arrancar el proyecto. **El proyecto hay que arrancarlo cada vez que te pongas a programar.** Para ello ejecuta el comando:

```bash
npm start
```

Este comando:

- **Abre una ventana de Chrome y muestra tu página web**, al igual que hace el plugin de VS Code Live Server (Go live).
- También **observa** todos los ficheros que hay dentro de la carpeta `src/`, para que cada vez que modifiques un fichero **refresca tu página en Chrome**.
- También **procesa los ficheros** HTML, SASS / CSS y JS y los **genera y guarda en la carpeta `public/`**. Por ejemplo:
  - Convierte los ficheros SASS en CSS.
  - Combina los diferentes ficheros de HTML y los agrupa en uno o varios ficheros HTML.

Después de ejecutar `npm start` ya puedes empezar a editar todos los ficheros que están dentro de la carpeta `src/` y programar cómodamente.

### Pasos para publicar el proyecto en GitHub Pages:

Para generar aportaciones a nuestro proyecto para producción ejecuta el comando:

```bash
npm run docs
```

Y a continuación:

1. Sube a tu repo la carpeta `docs/` que se te acaba de generar.
1. Entra en la pestaña `settings` de tu repo.
1. Y en el apartado de GitHub Pages activa la opción **master branch /docs folder**.
1. Y ya estaría!!!

Además, los comandos:

```bash
npm run push-docs
```

o

```bash
npm run deploy
```

son un atajo que nos genera la versión de producción y hace push de la carpeta `docs/` del tirón. Te recomendamos ver el fichero `package.json` para aprender cómo funciona.

## Flujo de archivos con Gulp

Estas tareas de Gulp producen el siguiente flujo de archivos:

![Gulp flow](./gulp-flow.png)

## `gulpfile.js` y `config.json`

Nuestro **gulpfile.js** usa el fichero `config.json` de configuración con las rutas de los archivos a generar / observar.

De esta manera separarmos las acciones que están en `gulpfile.js` de la configuración de las acciones que están en `config.json`.

## Estructura de carpetas

La estructura de carpetas tiene esta pinta:

```
src
 ├─ api // los ficheros de esta carpeta se copian en public/api/
 |  └─ data.json
 ├─ images
 |  └─ logo.jpg
 ├─ js // los ficheros de esta carpeta se concatenan en el fichero main.js y este se guarda en public/main.js
 |  ├─ main.js
 |  └─ events.js
 ├─ scss
 |  ├─ components
 |  ├─ core
 |  ├─ layout
 |  └─ pages
 └─ html
    └─ partials
```

## Para recibir ayuda sobre nuestro proyecto.

No dudes en contactar con nosotras a través del formulario de la web.

## Agradecimientos.

A nuestros profes y compañeras de Adalab por sus feedbacks y recomendaciones.

