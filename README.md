# TrainZone

## Introducción del Proyecto

El proyecto busca dar respuesta a la necesidad del centro de entrenamiento TrainZone de tener un hueco en internet, donde se muestre los servicios que ofrecen, el equipo que conforma el centro y las distintas valoraciones y experiencias de los clientes.

Recordando el motivo principal de la web, era clave ofrecer un espacio de contacto y un widget que localice al centro en el mapa.

## Tecnologías Utilizadas

Para la creación del proyecto se utilizaron las siguientes herramientas y tecnologías, cada una en la fase correspondiente.

- Figma
- Git y GitHub
- Typescript
- Astro Framework
- Vercel
- Ionos (Dominio)

## Diseño en Figma

Se usó la herramienta de diseño Figma para hacer todo el diseño del interfaz de usuario correspondiente. Se buscaba un diseño limpio y claro que tuviera los colores corporativos y se viera de manera organizada por secciones la información relevante a mostrar.

Para ello nos centramos en tener un Hero principal donde establecer los elementos de navegación principales, de forma que fueran los más llamativo junto con el título de la Web. Seguidamente, se diseñó una sección para cada uno de los requisitos de información del centro, siempre manteniendo el mismo lenguaje de diseño minimalista, donde respire el contenido y con apariencia redondeada.

En las páginas de servicios y equipo, se usa la tendencia de diseño Bento, para mostrar la información de una forma visual. Y todo sin olvidar la adaptabilidad para distintos dispositivos.

[Prototipo de alta fidelidad en Figma >](https://www.figma.com/file/zsKnK0DEcB6BxOKwOK05aN/TrainZone?type=design&node-id=0%3A1&mode=design&t=ajzu1caT4KjcIpAo-1)

## Implementación con Astro Framework

Consideré que Astro era el framework que mejor se adaptaba a las necesidades del proyecto, ya que [TrainZone](https://trainzone.es), se trata de una página web completamente estática en la que simplemente se buscaba mostrar información. La idea es que fuera lo más eficiente posible de cara a tenerUna buena experiencia de usuario y un buen SEO.

Astro facilita mucho la experiencia de desarrollo. Su herramienta de auditoría es muy útil para ir solucionando problemas de accesibilidad y rendimiento. Y su forma de gestionar los estilos es muy sencilla ya que establecen en cada componente. Esto permite usar CSS puro sin ocupar archivos enormes durante el desarrollo.

El proyecto se estructuró de forma sencilla, componetizando cada una de las secciones y elementos recurrentes de la UI. Una de las decisiones tomadas fue introducir los código SVG de los distintos iconos en componentes, guardados en la carpeta `/icons`, de forma que fuera sencilla su reutilización.

```bash
/
  ├── public/
  │   ├── favicon.svg
  │   └── ...
  ├── src/
  │   ├── components/
  │   │   ├── icons/
  │   │   ├── Hero.astro
  │   │   └── ...
  │   ├── layouts/
  │   │   └── Layout.astro
  │   └── pages/
  │       ├── index.astro
  │       ├── services.astro
  │       └── team.astro
  └── package.json
```

### Comandos

Estos son los comandos para inicializar el proyecto:

| Command           | Action                                       |
| :---------------- | :------------------------------------------- |
| `npm install`     | Instalar dependencias                        |
| `npm run dev`     | Comienza un servidor local `localhost:4321`  |
| `npm run build`   | Construye tu build para producción `./dist/` |
| `npm run preview` | Previsualiza tu build localmente             |

## Despliegue en Vercel

Se escogió Vercel como herramienta para llevar a cabo el despliegue de la web. Esta herramienta ofrece una integración completa con Astro y es muy sencillo a la par que económico su uso.

Al estar el código de la web en un repositorio de GitHub y al haber configurado en Vercel el enlace con el mismo y el dominio, el despliegues a producción se hace de forma automática.

## Dominio en Ionos

Nuestro cliente contaba con el dominio `trainzone.es` en propiedad, a través del proveedor Ionos.
La configuración en el panel de Ionos fue rápida y sencilla.

## Futuras Mejoras

Si bien es un proyecto simple, que no da pie a muchas modificaciones, si hay algunos aspectos que podrían ser mejorados a futuro, siempre con el visto bueno del cliente.

- Sustitución de las imágenes de la página de servicios.
- Corrección de los colores verdosos para un mejor contraste con el texto.
- Llevar a cabo un estudio de experiencia de usuario.
- Usar logotipos con formatos vectoriales si se tuvieran.
- Implementar Tailwind para simplificar los estilos.

## Aprendizajes y Desafíos

Principalmente el aprendizaje es el poder haber trabajado con un cliente real y plasmar su idea de tal forma que sea fiel a las necesidades del negocio.
