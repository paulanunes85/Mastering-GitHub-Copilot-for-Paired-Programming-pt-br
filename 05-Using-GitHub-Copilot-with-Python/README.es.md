<header>

# Usando GitHub Copilot con Python

GitHub Copilot es la primera herramienta de desarrollador con IA a gran escala del mundo que acelera significativamente la escritura de código, proporcionando sugerencias de autocompletado mientras trabajas. En este módulo, nos enfocaremos en usar el poder de GitHub Copilot para aumentar la eficiencia de tu codificación en Python.

Como desarrollador, tu objetivo es aumentar la productividad y acelerar los procesos de codificación. GitHub Copilot actúa como tu programador en pareja con IA, ofreciendo sugerencias basadas en el contexto y los patrones de código. En este módulo, usarás GitHub Copilot con Codespaces para generar e implementar sugerencias de código de forma eficaz.

¡Prepárate para sumergirte en un escenario del mundo real! Modificarás un repositorio Python usando GitHub Copilot para crear un formulario HTML interactivo y un endpoint de API. Este proyecto te dará una experiencia valiosa en el desarrollo de una aplicación web Python que sirve una API HTTP, generando tokens pseudo-aleatorios para fines de identificación.

</header>

- **¿Para quién es esto?:** Desarrolladores, Ingenieros DevOps, Gerentes de desarrollo de software, Testers.
- **Lo que aprenderás:** Usar GitHub Copilot para crear código y añadir comentarios a tu trabajo.
- **Lo que construirás:** Archivos Python que tendrán código generado por la IA de Copilot para sugerencias de código y comentarios.
- **Prerrequisitos:** Para usar GitHub Copilot, debes tener una suscripción activa de GitHub Copilot Business o Enterprise. Regístrate para Copilot Free para VS Code solo para fines de entrenamiento [Copilot for free para VS Code](https://learn.microsoft.com/en-us/visualstudio/ide/copilot-free-plan?view=vs-2022).
- **Tiempo:** Este módulo puede completarse en menos de una hora.

Al final de este módulo, adquirirás las habilidades para:

- Crear indicaciones para generar sugerencias de GitHub Copilot
- Aplicar GitHub Copilot para mejorar tus proyectos.

## Lecturas previas requeridas:
- [Introducción a la ingeniería de prompts con GitHub Copilot](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [Usando GitHub Copilot con Python](https://learn.microsoft.com/en-us/training/modules/introduction-copilot-python/?WT.mc_id=academic-113596-abartolo)

## Requisitos

1. Habilita tu [servicio GitHub Copilot](https://github.com/github-copilot/signup)
1. Abre [este repositorio con Codespaces](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-python)

## 💪🏽 Ejercicio

**Haz clic derecho en el botón Codespaces a continuación para abrir tu Codespace en una nueva pestaña**
 
[![Abrir GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-python)

La API ya tiene un único endpoint para generar un token. Vamos a actualizar la API añadiendo un nuevo endpoint que acepta texto y devuelve una lista de tokens.

### 🛠 Paso 1: Añadir un modelo Pydantic

Ve al archivo `main.py`, navega hasta el final del código proporcionado, selecciona **Ctrl + I (PC)** o **Cmd + I (Mac)** y copia lo siguiente en el cuadro de chat de GitHub Copilot proporcionado para que pueda generar un modelo `Pydantic` para ti:

```
Create a Pydantic model so that I can use it in a new route that will accept JSON with text as a key which accepts a string.
```

```
Crea un modelo Pydantic para que pueda usarlo en una nueva ruta que aceptará JSON con texto como clave que acepta una cadena.
```

El modelo generado debería ser similar a este:

```python
    class TextData(BaseModel):
        text: str
```

> [!NOTA]
> Puedes ver algunas advertencias del linter en el editor (identificables con subrayados rojos punteados) que pueden ignorarse. Estos incluyen líneas largas o incluso nuevas líneas que no son necesarias. Siéntete libre de corregirlos, aunque esto no debería afectar la ejecución correcta de tu aplicación.

### 🔎 Paso 2: Generar un nuevo endpoint

A continuación, genera un nuevo endpoint con GitHub Copilot añadiendo el comentario en la parte inferior del archivo `main.py` bajo la última ruta.

```python
# Create a FastAPI endpoint that accepts a POST request with a JSON body containing a single field called "text" and returns a checksum of the text 
```

```python
# Crea un endpoint FastAPI que acepte una solicitud POST con un cuerpo JSON que contenga un único campo llamado "text" y devuelva un checksum del texto
```

Puedes recibir una sugerencia que usa un módulo o biblioteca que no se ha importado. Si esto ocurre, puedes pedir a GitHub Copilot que te ayude a importar el módulo correcto seleccionando el código generado y usando Command+I (Apple) o Control+I (Windows) y añadiendo un prompt para añadir las importaciones faltantes. Este pequeño pop-up se llama chat en línea y es otra manera de interactuar con GitHub Copilot.

### 🐍 Paso 3: Explicar el código

La ruta `generate()` crea un ID de token pseudo-aleatorio usando una única línea que puede ser difícil de entender completamente. Selecciona toda la función, haz clic derecho en la selección, selecciona el elemento de menú Copilot y luego la opción _"Explain This"_. La interfaz de chat de GitHub Copilot se abrirá a la izquierda y proporcionará una explicación.

Finalmente, verifica que el nuevo endpoint está funcionando, probándolo accediendo al endpoint `/docs` y confirmando que el endpoint aparece.


🚀 ¡Felicidades, a través del ejercicio, no solo has usado Copilot para generar código, sino que también lo has hecho de una manera interactiva y divertida! Puedes usar GitHub Copilot no solo para generar código, sino también para escribir documentación, probar tus aplicaciones y mucho más.


### 💡 Paso 4: Usando Comandos de Barra

Ahora que has usado GitHub Copilot para generar y explicar código, también puedes explorar algunos otros enfoques alternativos para realizar tareas de desarrollador. Estos desafíos adicionales te ayudarán a profundizar en otras características de GitHub Copilot más allá de las que ya conoces. Para estos desafíos adicionales, usarás la interfaz de chat. Haz clic en el icono de chat de GitHub Copilot en la barra lateral izquierda si aún no está abierto.


**Generar documentación**
 
Con `main.py` abierto, usa la interfaz de chat con el siguiente texto:

```
/docs I need to document the routes for these API Routes. Help me produce documentation I can put in the README.md file of this project
```

```
/docs Necesito documentar las rutas para estas rutas de API. Ayúdame a producir documentación que pueda poner en el archivo README.md de este proyecto
```

La parte `/docs` del prompt se llama _"comando de barra"_ y es una característica específica de GitHub Copilot que permite escribir documentación. Si los resultados parecen buenos, añádelos a una nueva sección de tu archivo README.md.


**Generar pruebas**
 
El código actual no tiene pruebas. Para este desafío, usarás el comando de barra `/tests`. Con `main.py` abierto, usa la interfaz de chat con el siguiente prompt:

```
/tests help me write a test for the generate() route using the FastAPI test client and the Pytest framework. Help me understand where I should put the test file, how to add the Pytest dependency to my project, and how to run the tests
```

```
/tests ayúdame a escribir una prueba para la ruta generate() usando el cliente de prueba FastAPI y el framework Pytest. Ayúdame a entender dónde debo colocar el archivo de prueba, cómo añadir la dependencia Pytest a mi proyecto y cómo ejecutar las pruebas
```

El comando de barra `/tests` te guiará en la escritura de una nueva prueba para tu ruta y te proporcionará todo lo que necesitas para verificar tu trabajo.


**Desafío del Workspace**
 
Finalmente, tendrás la oportunidad de usar un agente. Los agentes son una característica especial de GitHub Copilot en Visual Studio Code que permiten que un contexto específico se comparta con GitHub Copilot. Para este desafío final, usarás el agente `@workspace`, que incluye archivos del espacio de trabajo actual para proporcionar más contexto. Resolverás un problema relacionado con cómo ejecutar toda la aplicación. En este caso, mejorarás el README.md para obtener más detalles que abarcan varios archivos. Usar `@workspace` ayuda a proporcionar más contexto sin necesidad de abrir muchos archivos.

Para este desafío final, no necesitas tener ningún archivo abierto. Usa el siguiente prompt en la ventana de chat de GitHub Copilot:

```
@workspace I want to provide instructions on how to run this application using the uvicorn webserver, I also need to provide instructions on how to install the dependencies properly and what are some characteristics of the FastAPI framework. I will use this to improve the README.md file
```

```
@workspace Quiero proporcionar instrucciones sobre cómo ejecutar esta aplicación usando el servidor web uvicorn, también necesito proporcionar instrucciones sobre cómo instalar las dependencias correctamente y cuáles son algunas características del framework FastAPI. Usaré esto para mejorar el archivo README.md
```

El resultado debería ser una explicación muy buena sobre FastAPI, cómo ejecutar la aplicación y cómo instalar las dependencias. Un informe en la parte superior de la respuesta puede incluir todas las referencias utilizadas para determinar qué archivos necesitaba usar para proporcionar el contexto correcto para GitHub Copilot.


## Avisos Legales

Microsoft y cualquier colaborador te otorgan una licencia para la documentación de Microsoft y otros contenidos en este repositorio bajo la [Licencia Pública Internacional Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/legalcode),
ver [LICENSE](LICENSE) y te otorgan una licencia para cualquier código en el repositorio bajo la [Licencia MIT](https://opensource.org/licenses/MIT), consulta
[LICENSE-CODE](LICENSE-CODE)

Microsoft, Windows, Microsoft Azure y/u otros productos y servicios de Microsoft mencionados en la documentación pueden ser marcas comerciales o marcas registradas de Microsoft en los Estados Unidos y/u otros países. Las licencias de este proyecto no te otorgan derechos para usar ningún nombre, logotipo o marca comercial de Microsoft. Las directrices generales de marcas de Microsoft se pueden encontrar en http://go.microsoft.com/fwlink/?LinkID=254653.

La información de privacidad se puede encontrar en https://privacy.microsoft.com/en-us/

Microsoft y cualquier colaborador se reservan todos los demás derechos, ya sea bajo sus respectivos derechos de autor, patentes o marcas comerciales, ya sea por implicación, impedimento legal o de otro modo. 