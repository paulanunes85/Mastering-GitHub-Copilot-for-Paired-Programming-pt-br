<header>

# Usando Características Avanzadas de GitHub Copilot

GitHub Copilot ofrece más que solo sugerencias de código. Como Ingeniero de Software, frecuentemente te encontrarás intentando entender el código existente y mejorarlo con documentación, pruebas y automatización.

En este módulo, usarás las características avanzadas de GitHub Copilot que te permitirán trabajar interactivamente con tu código y aplicar sugerencias y conocimientos de forma eficiente.

Usarás una API HTTP existente basada en Python para hacer cambios, correcciones de errores, documentación y pruebas para un nuevo endpoint que implementarás.

</header>

- **¿Para quién es esto?:** Desarrolladores, Ingenieros DevOps, Gerentes de desarrollo de software, Testers.
- **Lo que aprenderás:** Usar características avanzadas de GitHub Copilot para probar, documentar y trabajar con código.
- **Lo que construirás:** Una nueva ruta de API HTTP, junto con documentación y pruebas para verificar su corrección.
- **Prerrequisitos:** Para usar GitHub Copilot, debes tener una suscripción activa de GitHub Copilot Business o Enterprise. Regístrate para Copilot Free para VS Code solo para fines de entrenamiento [Copilot for free para VS Code](https://learn.microsoft.com/en-us/visualstudio/ide/copilot-free-plan?view=vs-2022).
- **Tiempo:** Este módulo puede completarse en menos de una hora.

Al final de este módulo, adquirirás las habilidades para:

- Usar características avanzadas de GitHub Copilot, como chat en línea, comandos de barra y agentes.
- Interactuar con GitHub Copilot con un contexto más profundo sobre tu proyecto y hacer preguntas sobre él.

## Lecturas previas requeridas:
- [Introducción a la ingeniería de prompts con GitHub Copilot](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [Usando características avanzadas de GitHub Copilot](https://learn.microsoft.com/training/modules/advanced-github-copilot/?WT.mc_id=academic-113596-abartolo)

## Requisitos

1. Habilita tu [servicio GitHub Copilot](https://github.com/github-copilot/signup)
1. Abre [este repositorio con Codespaces](https://codespaces.new/MicrosoftDocs/mslearn-advanced-copilot)

## 💪🏽 Ejercicio

**Haz clic derecho en el botón Codespaces a continuación para abrir tu Codespace en una nueva pestaña**
 
[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/MicrosoftDocs/mslearn-copilot-codespaces-python)

La API actual no está exponiendo country/{country}, que necesita ser implementado para listar ciudades. La ruta debe permitir solo solicitudes HTTP GET con una respuesta JSON proporcionando información sobre los máximos y mínimos históricos para ese país, ciudad y mes específico.

Como en cualquier implementación, esta adición debe incluir al menos una función de prueba para funcionar con el ejecutor pytest y el framework de prueba.

### 🛠 Paso 1: Añadir una nueva ruta 

En nuestro primer ejercicio, crearemos una nueva ruta en nuestra API. Ve al archivo `main.py` y, usando el chat en línea con el siguiente comando `ctrl + i` (en Windows) o `cmd + i` (en Mac), pide a GitHub Copilot que te ayude a crear una nueva API que muestre las ciudades de un país.

Usa el siguiente prompt en el chat en línea:


```
Create a new route that exposes the cities of a country.
```
```
Crea una nueva ruta que exponga las ciudades de un país.
```

Este prompt debería proporcionar algo similar a esto:


```python
# Create a new route that exposes the cities of a country:
@app.get('/countries/{country}')
def cities(country: str):
    return list(data[country].keys())

```
```python
# Crea una nueva ruta que exponga las ciudades de un país:
@app.get('/countries/{country}')
def cities(country: str):
    return list(data[country].keys())

```


> [!NOTA]
> Prueba tu nueva ruta y refina tu prompt hasta que el resultado sea el deseado.

### 🔎 Paso 2: Crear una prueba
Ahora que has creado una nueva ruta, vamos a crear una prueba con Copilot Chat para esa ruta que utiliza España como país. Recuerda seleccionar tu código y pedir a Copilot Chat que te ayude con esta API específica que acabamos de crear.

Usa el siguiente prompt con GitHub Copilot Chat:

```
/tests help me to create a new test for this route that uses Spain as the country.
```
```
/tests ayúdame a crear una nueva prueba para esta ruta que utiliza España como país.
```

![Copilot Chat image example](https://raw.githubusercontent.com/MicrosoftDocs/mslearn-advanced-copilot/main/images/ideascopilot.png)


Después de que Copilot te ayude a crear tu prueba, pruébala. Si no está funcionando como esperabas, siéntete libre de compartir esos detalles con Copilot en el chat. Por ejemplo:

```
This test is not quite right, it is not including cities that doesn't exist. Only Seville is part of the API.
```
```
Esta prueba no está del todo bien, no está incluyendo ciudades que no existen. Solo Sevilla forma parte de la API.
```

Debería proporcionar otra solución. Continúa intentándolo hasta obtener el resultado deseado.

### 🐍 Paso 3: Usar un agente para escribir la documentación del proyecto
Durante este paso, usaremos un agente (workspace) para escribir la documentación del proyecto sobre cómo ejecutarlo. En GitHub Copilot Chat, intentaremos el siguiente prompt:

`> @workspace help me to use an agent to write the project documentation on how to run it .`

`> @workspace ayúdame a usar un agente para escribir la documentación del proyecto sobre cómo ejecutarlo.`

Finalmente, verifica que el nuevo endpoint esté funcionando probándolo accediendo al endpoint `/docs` y confirmando que el endpoint aparece.


### 💡 Paso 4: Usando Comandos de Barra

Ahora que has usado GitHub Copilot para generar y explicar código, también puedes explorar algunos otros enfoques alternativos para realizar tareas de desarrollador. Estos desafíos adicionales te ayudarán a profundizar en otras características de GitHub Copilot más allá de las que ya conoces. Para estos desafíos adicionales, usarás la interfaz de chat. Haz clic en el icono de GitHub Copilot Chat en la barra lateral izquierda si aún no está abierto.

🚀 ¡Felicidades, a través del ejercicio, has usado GitHub Copilot con muchas características diferentes que te permitirán trabajar mejor con diferentes proyectos. Has usado interactivamente algunas características para escribir pruebas, documentación y descubrir más sobre el código existente.

## Avisos Legales
 
Microsoft y cualquier colaborador te otorgan una licencia para la documentación de Microsoft y otros contenidos en este repositorio bajo la [Licencia Pública Internacional Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/legalcode),
ver [LICENSE](LICENSE) y te otorgan una licencia para cualquier código en el repositorio bajo la [Licencia MIT](https://opensource.org/licenses/MIT), consulta
[LICENSE-CODE](LICENSE-CODE)
 
Microsoft, Windows, Microsoft Azure y/u otros productos y servicios de Microsoft mencionados en la documentación pueden ser marcas comerciales o marcas registradas de Microsoft en los Estados Unidos y/u otros países. Las licencias de este proyecto no te otorgan derechos para usar ningún nombre, logotipo o marca comercial de Microsoft. Las directrices generales de marcas de Microsoft se pueden encontrar en http://go.microsoft.com/fwlink/?LinkID=254653.
 
La información de privacidad se puede encontrar en https://privacy.microsoft.com/en-us/
 
Microsoft y cualquier colaborador se reservan todos los demás derechos, ya sea bajo sus respectivos derechos de autor, patentes o marcas comerciales, ya sea por implicación, impedimento legal o de otro modo. 