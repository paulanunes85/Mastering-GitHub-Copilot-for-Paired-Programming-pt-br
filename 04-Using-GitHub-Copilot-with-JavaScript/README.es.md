<header>

# Usando GitHub Copilot con JavaScript

En este módulo, continuaremos explorando las capacidades de GitHub Copilot y aprenderemos cómo usarlo para mejorar tu experiencia de codificación. Imagina escribir código más rápido y con menos esfuerzo—GitHub Copilot hace esto realidad al generar sugerencias basadas en el contexto de tus comentarios y código.

Como desarrollador en busca de mayor productividad, te embarcarás en un viaje para dominar las capacidades de GitHub Copilot, enfocándote en su aplicación en JavaScript. Al final del módulo, habrás ganado experiencia en crear indicaciones que generan sugerencias valiosas usando la extensión de GitHub Copilot en Visual Studio Code. Eleva tus habilidades de codificación al usar GitHub Copilot para mejorar un proyecto JavaScript, experimentando de primera mano cómo este programador en pareja con IA ofrece sugerencias de autocompletado, transformando tu flujo de trabajo de desarrollo.

Al dominar GitHub Copilot, no solo configurarás repositorios en Codespaces, sino que también utilizarás eficientemente esta herramienta de IA para mejorar tus proyectos de codificación. ¡Prepárate para revolucionar tu experiencia de codificación y aumentar tu productividad en esta dinámica aventura de aprendizaje!

</header>


- **¿Para quién es esto?:** Desarrolladores, Ingenieros DevOps, Gerentes de desarrollo de software, Testers.
- **Lo que aprenderás:** Usar GitHub Copilot para crear código y añadir comentarios a tu trabajo.
- **Lo que construirás:** Archivos JavaScript que tendrán código generado por la IA de Copilot para sugerencias de código y comentarios.
- **Prerrequisitos:** Para usar GitHub Copilot, debes tener una suscripción activa de GitHub Copilot Business o Enterprise. Regístrate para Copilot Free para VS Code solo para fines de entrenamiento [Copilot for free para VS Code](https://learn.microsoft.com/en-us/visualstudio/ide/copilot-free-plan?view=vs-2022).
- **Tiempo:** Este módulo puede completarse en menos de una hora.


Al final de este módulo, adquirirás las habilidades para:

- Crear indicaciones para generar sugerencias de GitHub Copilot
- Aplicar GitHub Copilot para mejorar tus proyectos.


## Lecturas previas requeridas:
- [Introducción a la ingeniería de prompts con GitHub Copilot](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [Usando GitHub Copilot con JavaScript](https://learn.microsoft.com/training/modules/introduction-copilot-javascript/?WT.mc_id=academic-113596-abartolo)


## Requisitos

1. Habilita tu [servicio GitHub Copilot](https://github.com/github-copilot/signup)
1. Abre [este repositorio con Codespaces](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-javascript?quickstart=1)



## 💪🏽 Ejercicio

**Haz clic derecho en el botón Codespaces a continuación para abrir tu Codespace en una nueva pestaña**

[![Abrir GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=526682619)

En este modelo de portafolio, tenemos una aplicación web basada en React lista para que la personalices y despliegues fácilmente usando solo tu navegador web.

**Nota:** Por favor, ignora las instrucciones proporcionadas dentro del GitHub Codespace. Para estos laboratorios, asegúrate de seguir las instrucciones que se encuentran aquí.


### 🛠 Paso 1: Personaliza la aplicación web

Personaliza el portafolio con tus propios enlaces. Ve a src/App.jsx y actualiza siteProps con tu información. La variable siteProps es un objeto JavaScript que contiene pares de clave y valor utilizados para personalizar el sitio, debe verse así:

```javascript
const siteProps = {
  name: "Alexandrie Grenier",
  title: "Web Designer & Content Creator",
  email: "alex@example.com",
  gitHub: "microsoft",
  instagram: "microsoft",
  linkedIn: "satyanadella",
  medium: "",
  twitter: "microsoft",
  youTube: "Code",
};
```
### 📖 Paso 2: Explica el código

Ahora usemos el comando de barra para explicar lo que hace una parte del código. Destaca el siguiente código:

```javascript
};

const primaryColor = "#4E567E";
const secondaryColor = "#D2F1E4";

const App = () => {
  return (
    <div id="main">
      <Header />
      <Home name={siteProps.name} title={siteProps.title} />
      <About />
      <Portfolio />
      <Footer {...siteProps} primaryColor={primaryColor} secondaryColor={secondaryColor} />
    </div>
  );
};
```
Una vez destacado, presiona Ctrl + I (Windows) o Cmd + I (Mac) y escribe /explain. Deberías recibir una respuesta en la ventana de Copilot Chat similar a esta:

```
This JavaScript code is written in React, a popular library for building user interfaces. The code defines a functional component named App. The App component is the root component of your application. It's where all other components (Header, Home, About, Portfolio, Footer) are being called and rendered. The App component returns a JSX (JavaScript XML) structure, which looks similar to HTML. This JSX structure defines what the App component should render on the screen. In the JSX, there is a div with an id of "main". Inside this div, several components are being rendered: Header, Home, About, Portfolio, and Footer. The Home component is being passed two props: name and title, both of which are properties of the siteProps object. The Footer component is being passed several props. The ...siteProps syntax is using the JavaScript spread operator to pass all properties of siteProps as separate props. In addition to the siteProps, two more props are being passed: primaryColor and secondaryColor. These are defined as constants at the top of the file. Remember, props (short for properties) in React are how components talk to each other. If you think of components as functions, then props are the arguments to these functions. They are passed from the parent component (in this case, App) to the child components (Header, Home, About, Portfolio, Footer).
```
Este código JavaScript está escrito en React, una biblioteca popular para construir interfaces de usuario. El código define un componente funcional llamado App. El componente App es el componente raíz de tu aplicación. Es donde todos los demás componentes (Header, Home, About, Portfolio, Footer) son llamados y renderizados. El componente App devuelve una estructura JSX (JavaScript XML), que se parece a HTML. Esta estructura JSX define lo que el componente App debe renderizar en la pantalla. En el JSX, hay un div con un id de "main". Dentro de este div, varios componentes están siendo renderizados: Header, Home, About, Portfolio y Footer. Al componente Home se le están pasando dos props: name y title, ambos son propiedades del objeto siteProps. Al componente Footer se le están pasando varios props. La sintaxis ...siteProps está usando el operador spread de JavaScript para pasar todas las propiedades de siteProps como props separados. Además de siteProps, se están pasando dos props más: primaryColor y secondaryColor. Estos están definidos como constantes en la parte superior del archivo. Recuerda, props (abreviatura de propiedades) en React son cómo los componentes se comunican entre sí. Si piensas en los componentes como funciones, entonces props son los argumentos de estas funciones. Se pasan del componente padre (en este caso, App) a los componentes hijos (Header, Home, About, Portfolio, Footer).
```

Profundicemos un poco más. Observa cómo Copilot Chat ahora proporciona una sugerencia de pregunta de seguimiento para que hagas. Haz clic en la pregunta sugerida por GitHub Copilot que se encuentra en la parte inferior de la ventana, generalmente comenzando con "¿Cuál es el propósito..." y revisa la respuesta proporcionada. Por ejemplo, si la pregunta sugerida por GitHub Copilot es la siguiente:

¿Cuál es el propósito de usar props en componentes React?

Deberías obtener una respuesta similar a esta:

```
Props (short for properties) in React are used for passing data from one component to another, just like function arguments. They are read-only and help to make components reusable and dynamic. In your code, for example, the Home component is passed name and title as props. This means that the Home component can use these values to display dynamic content. The Footer component is also passed several props, including all properties of siteProps and the primaryColor and secondaryColor constants. Here's an analogy: think of a component as a custom HTML element and props as the attributes of that element. Just like you can pass different attributes to an HTML element (like <img src="image.jpg" alt="An image">), you can pass different props to a React component (like <Home name="John" title="Developer" />). This makes your components more flexible and reusable. For instance, you could use the same Home component with different props to display different content.
```
```
Props (abreviatura de propiedades) en React se utilizan para pasar datos de un componente a otro, al igual que los argumentos de función. Son de solo lectura y ayudan a hacer que los componentes sean reutilizables y dinámicos. En tu código, por ejemplo, al componente Home se le pasan name y title como props. Esto significa que el componente Home puede usar estos valores para mostrar contenido dinámico. Al componente Footer también se le pasan varios props, incluidas todas las propiedades de siteProps y las constantes primaryColor y secondaryColor. Aquí hay una analogía: piensa en un componente como un elemento HTML personalizado y en props como los atributos de ese elemento. Al igual que puedes pasar diferentes atributos a un elemento HTML (como <img src="image.jpg" alt="Una imagen">), puedes pasar diferentes props a un componente React (como <Home name="John" title="Developer" />). Esto hace que tus componentes sean más flexibles y reutilizables. Por ejemplo, podrías usar el mismo componente Home con diferentes props para mostrar contenido diferente.
```

Habrás notado que después de hacer clic en la pregunta sugerida en la ventana de Copilot Chat, usó un comando similar al siguiente para hacer la pregunta:

```
@workspace /explain ¿Cuál es el propósito de usar props en componentes React?
```

El agente @workspace, como Copilot, completa detalles ausentes, ayudando cuando los humanos omiten o no describen completamente todo lo que ven. Cuando se le solicita, Copilot adopta un enfoque diferente. En lugar de responder inmediatamente, primero examina los archivos y carpetas en el espacio de trabajo en etapas:

1. Verifica los nombres de los archivos/carpetas para ver cuáles pueden ser relevantes.
2. Lee el contenido de los archivos, a veces en su totalidad, a veces parcialmente debido a límites de memoria.
3. Crea contexto a partir de la información recopilada.
4. Responde, utilizando tanto el contexto del prompt como la información que ha reunido.


### 🔎 Paso 3: Animar los iconos de redes sociales con un prompt

Una animación puede hacer que la sección de redes sociales sea más atractiva. Pide ayuda a Copilot para animar los iconos. Ve al final del archivo y escribe el siguiente prompt en el archivo src/styles.css:

```css
/* add an amazing animation to the social icons */
```
```css
/* añade una animación increíble a los iconos sociales */
```

La sugerencia de Copilot debería ser similar a la siguiente:

```css
img.socialIcon:hover {
  animation: bounce 0.5s;
  animation-iteration-count: infinite;
}

@keyframes bounce {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
```

### 🚀 Paso 4: Descubre cómo ejecutar la aplicación

Abre el chat de GitHub Copilot haciendo clic en el icono de chat en la barra lateral izquierda y usa la sección de entrada para preguntar lo siguiente:

```
@workspace Quiero entender cómo puedo ejecutar esta aplicación React
```

Los prompts usan '@workspace', que es una característica especial del chat de GitHub Copilot que permite incluir más contexto para una respuesta más completa. Prueba otras consultas usando el panel de chat para un flujo de trabajo más interactivo.

### Conclusión

Tu sitio ya debería estar ejecutándose en tu Codespace, y el cambio se recargará automáticamente en la página. Para verlos, pasa el ratón sobre uno de tus iconos de redes sociales en el pie de página para ver la magia.

**Nota:** Actualiza la ventana del navegador del Codespace si los efectos de hover no funcionan.

¡Felicidades, a través del ejercicio, has usado GitHub Copilot para generar código y también lo has hecho de una manera interactiva y divertida! Puedes usar GitHub Copilot no solo para generar código, sino también para escribir documentación, probar tus aplicaciones y mucho más.

## Avisos Legales
 
Microsoft y cualquier colaborador te otorgan una licencia para la documentación de Microsoft y otros contenidos en este repositorio bajo la [Licencia Pública Internacional Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/legalcode),
ver [LICENSE](LICENSE) y te otorgan una licencia para cualquier código en el repositorio bajo la [Licencia MIT](https://opensource.org/licenses/MIT), consulta
[LICENSE-CODE](LICENSE-CODE)
 
Microsoft, Windows, Microsoft Azure y/u otros productos y servicios de Microsoft mencionados en la documentación pueden ser marcas comerciales o marcas registradas de Microsoft en los Estados Unidos y/u otros países. Las licencias de este proyecto no te otorgan derechos para usar ningún nombre, logotipo o marca comercial de Microsoft. Las directrices generales de marcas de Microsoft se pueden encontrar en http://go.microsoft.com/fwlink/?LinkID=254653.
 
La información de privacidad se puede encontrar en https://privacy.microsoft.com/en-us/
 
Microsoft y cualquier colaborador se reservan todos los demás derechos, ya sea bajo sus respectivos derechos de autor, patentes o marcas comerciales, ya sea por implicación, impedimento legal o de otro modo. 