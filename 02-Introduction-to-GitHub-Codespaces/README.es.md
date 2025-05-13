<header>

# Introducción a GitHub Codespaces

Bienvenido al emocionante mundo de GitHub Codespaces, tu recurso de codificación basado en la nube. En este módulo, nos sumergiremos en el reino de los entornos de desarrollo instantáneos y basados en la nube, revolucionando la manera en que abordas la codificación. GitHub Codespaces ofrece una experiencia integrada, proporcionando un contenedor equipado con los lenguajes, herramientas y utilidades esenciales para el desarrollo.

A lo largo de este viaje de aprendizaje, nos embarcaremos en el descubrimiento del ciclo de vida y los procesos de Codespaces. Descubre el poder de personalizar la configuración de tu Codespace para satisfacer tus preferencias y requisitos únicos. Para solidificar tu comprensión, cerraremos el módulo con un ejercicio práctico, permitiéndote flexionar tus músculos de codificación dentro del entorno de GitHub Codespaces.

Imagina un entorno de desarrollo completamente configurado a tu alcance, accesible desde cualquier computadora con conexión a internet. GitHub Codespaces abre la puerta a una nueva era de codificación colaborativa y flexible. ¡Vamos a sumergirnos y desbloquear todo el potencial del desarrollo basado en la nube con GitHub Codespaces!

</header>

- **¿Para quién es esto?:** Desarrolladores, Ingenieros DevOps, Gerentes de Ingeniería, Gerentes de Producto.
- **Lo que aprenderás:** Cómo crear un codespace, enviar código desde un codespace, seleccionar una imagen personalizada y personalizar un codespace.
- **Lo que construirás:** Un codespace con archivos devcontainer.json, personalizaciones y customizaciones.
- **Prerrequisitos:** Necesitarás saber lo siguiente:
  - Uso de Visual Studio Code, [Visual Studio Code Docs](https://code.visualstudio.com/docs).
  - Comprensión del uso de GitHub o finalización del módulo anterior [Introducción a GitHub](https://github.com/paulanunes85/Mastering-GitHub-Copilot-for-Paired-Programming/tree/main/01-Introduction-to-GitHub/README.es.md).
- **Tiempo:** Este curso puede completarse en menos de una hora.

Al final de este módulo, serás capaz de:

1. Describir GitHub Codespaces.
2. Explicar el ciclo de vida de GitHub Codespaces y cómo realizar cada etapa.
3. Definir las diferentes personalizaciones que puedes hacer en GitHub Codespaces.


## Lecturas previas requeridas: 

- [Codifica con GitHub Codespaces](https://learn.microsoft.com/training/modules/code-with-github-codespaces/?WT.mc_id=academic-113596-abartolo)
- ¿Qué es GitHub Codespaces? (Lista de reproducción de videos a continuación)
- [![¿Qué es Codespaces?](https://img.youtube.com/vi/ozuDPmcC1io/0.jpg)](https://www.youtube.com/watch?v=ozuDPmcC1io&list=PLmsFUfdnGr3wTl-NCblzcrEv2lFSX975-)



### Cómo iniciar este curso

<!-- For start course, run in JavaScript:
'https://github.com/new?' + new URLSearchParams({
  template_owner: 'skills',
  template_name: 'code-with-codespaces',
  owner: '@me',
  name: 'skills-code-with-codespaces',
  description: 'My clone repository',
  visibility: 'public',
}).toString()
-->

[![Iniciar Curso](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=skills&template_name=code-with-codespaces&owner=%40me&name=skills-code-with-codespaces&description=My+clone+repository&visibility=public)

1. Haz clic derecho en **Iniciar curso** y abre el enlace en una nueva pestaña.
2. En la nueva pestaña, la mayoría de los campos se completarán automáticamente para ti.
   - Para el propietario, elige tu cuenta personal o una organización para alojar el repositorio.
   - Recomendamos crear un repositorio público, ya que los repositorios privados [utilizan minutos de Actions](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions?WT.mc_id=academic-113596-abartolo).
   - Desplázate hacia abajo y haz clic en el botón **Crear repositorio** en la parte inferior del formulario.
3. Después de crear tu nuevo repositorio, espera unos 20 segundos y actualiza la página. Sigue las instrucciones paso a paso en el README del nuevo repositorio.

## Avisos Legales
 
Microsoft y cualquier colaborador te otorgan una licencia para la documentación de Microsoft y otros contenidos en este repositorio bajo la [Licencia Pública Internacional Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/legalcode),
ver [LICENSE](LICENSE) y te otorgan una licencia para cualquier código en el repositorio bajo la [Licencia MIT](https://opensource.org/licenses/MIT), consulta
[LICENSE-CODE](LICENSE-CODE)
 
Microsoft, Windows, Microsoft Azure y/u otros productos y servicios de Microsoft mencionados en la documentación pueden ser marcas comerciales o marcas registradas de Microsoft en los Estados Unidos y/u otros países. Las licencias de este proyecto no te otorgan derechos para usar ningún nombre, logotipo o marca comercial de Microsoft. Las directrices generales de marcas de Microsoft se pueden encontrar en http://go.microsoft.com/fwlink/?LinkID=254653.
 
La información de privacidad se puede encontrar en https://privacy.microsoft.com/en-us/
 
Microsoft y cualquier colaborador se reservan todos los demás derechos, ya sea bajo sus respectivos derechos de autor, patentes o marcas comerciales, ya sea por implicación, impedimento legal o de otro modo.
<!--
<footer>

  <<< Author notes: Footer >>>
  Add a link to get support, GitHub status page, code of conduct, license link.
-->

---


Obtén ayuda: [Publica en nuestro tablón de discusión](https://github.com/orgs/skills/discussions/categories/introduction-to-github) &bull; [Revisa la página de estado de GitHub](https://www.githubstatus.com/) 