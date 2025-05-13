<header>

# Usando GitHub Copilot con C#

GitHub Copilot es la primera herramienta de desarrollador con IA a gran escala del mundo que acelera significativamente la escritura de código, proporcionando sugerencias de autocompletado mientras trabajas. En este módulo, nos enfocaremos en usar el poder de GitHub Copilot para aumentar la eficiencia de tu codificación en C#.

Como desarrollador, tu objetivo es aumentar la productividad y acelerar los procesos de codificación. GitHub Copilot actúa como tu programador en pareja con IA, ofreciendo sugerencias basadas en el contexto y los patrones de código. Al final de este módulo, no solo sabrás cómo configurar GitHub Copilot en Codespaces, sino también cómo generar e implementar sugerencias de código de forma eficaz.

¡Prepárate para sumergirte en un escenario del mundo real! Modificarás un repositorio C# usando GitHub Copilot para crear un endpoint de API. Este proyecto te dará una experiencia valiosa en el desarrollo de una aplicación web C# que sirve una API HTTP, generando información de previsión del tiempo pseudo-aleatoria.


</header>

- **¿Para quién es esto?:** Desarrolladores, Ingenieros DevOps, Gerentes de desarrollo de software, Testers.
- **Lo que aprenderás:** Cómo usar GitHub Copilot para crear código y añadir comentarios a tu trabajo.
- **Lo que construirás:** Archivos C# que tendrán código generado por la IA de Copilot para sugerencias de código y comentarios.
- **Prerrequisitos:** Para usar GitHub Copilot, debes tener una suscripción activa de GitHub Copilot Business o Enterprise. Regístrate para Copilot Free para VS Code solo para fines de entrenamiento [Copilot for free para VS Code](https://learn.microsoft.com/en-us/visualstudio/ide/copilot-free-plan?view=vs-2022).
- **Tiempo:** Este curso puede completarse en menos de una hora.

Al final de este módulo, adquirirás las habilidades para:

- Crear indicaciones para generar sugerencias de GitHub Copilot
- Aplicar GitHub Copilot para mejorar tus proyectos.

## Lecturas previas requeridas:
- [Introducción a la ingeniería de prompts con GitHub Copilot](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot?WT.mc_id=academic-113596-abartolo)

- [¿Qué es la extensión GitHub Copilot para Visual Studio?](https://learn.microsoft.com/en-us/visualstudio/ide/visual-studio-github-copilot-extension?view=vs-2022&WT.mc_id=academic-113596-abartolo)

## Requisitos

1. Habilita tu [servicio GitHub Copilot](https://github.com/github-copilot/signup)

1. Familiarízate con [usar repositorio con Codespaces](https://github.com/github/dotnet-codespaces)

## 💪🏽 Ejercicio

**Haz clic derecho en el botón Codespaces a continuación para abrir tu Codespace en una nueva pestaña**
 
[![Abrir en GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/github/dotnet-codespaces)

El repositorio **"GitHub Codespaces ♥️ .NET 8"** construye una API de Previsión del Tiempo usando APIs Mínimas, abre Swagger para que puedas llamar y probar la API y muestra los datos en una aplicación web usando Blazor con .NET 8.

Vamos a revisar los pasos para actualizar la aplicación BackEnd de Previsión del Tiempo añadiendo un nuevo endpoint que solicita una ubicación específica y devuelve la previsión del tiempo para esa ubicación.


### 🗒️ (Paso Opcional 1): Familiarízate con el repositorio "GitHub Codespaces ♥️ .NET 8"

Una vez que abras el repositorio en Codespaces, encontrarás una nueva ventana del navegador con un Codespace totalmente funcional. Todo en este repositorio está contenido dentro de este único Codespace. Por ejemplo, en el panel del explorador, podemos ver el código principal para el proyecto BackEnd y el proyecto FrontEnd.

![Nuevo Codespace con el repositorio en ejecución](./005OpenRepoInCodeSpaces.png)

Para ejecutar el proyecto BackEnd, ve al panel "Run and Debug" y selecciona el proyecto "BackEnd".

![Abrir program.cs en el proyecto BackEnd](./006RunBackEndProject.png)

Inicia la depuración del proyecto seleccionado. El proyecto de la API de Previsión del Tiempo, nuestro proyecto BackEnd, ahora estará en ejecución en el puerto 8080. Podemos copiar la URL publicada del panel **Ports**.

![Copiar la URL de la aplicación desde el panel de puertos](./007ProjectRunningOpenInNewTab.png)

La aplicación BackEnd publicó un endpoint llamado `weatherforecast` que genera datos de previsión aleatorios. Para probar la aplicación en ejecución, puedes añadir `/weatherforecast` a la URL publicada. La URL final debe ser similar a esta:


```bash
https://< tu url>.app.github.dev/weatherforecast
```

La aplicación en ejecución en un navegador debería verse así:

![probar ejecución de la API](./008TestRunningApi.png)

Ahora vamos a añadir un punto de interrupción en nuestra aplicación para depurar cada llamada a la API. Ve al archivo `Program.cs` en el proyecto BackEnd. El archivo está en la siguiente ruta `SampleApp\BackEnd\Program.cs`.

Añade un punto de interrupción en la línea 24 (presiona F9) y actualiza el navegador con la URL para probar el endpoint. El navegador no debería mostrar la previsión del tiempo, y en el Editor de Visual Studio podemos ver cómo la ejecución del programa se ha pausado en la línea 24.

![depurar la aplicación en ejecución.](./009DebugBackEndDemo.png)

Presionando F10, podemos depurar paso a paso hasta la línea 32, donde podemos ver los valores generados. La aplicación debe haber generado valores de previsión del tiempo para los próximos 5 días. La variable `forecast` contiene un array con esos valores.

![depurar la aplicación en ejecución.](./010DebugForecastValue.png)

Puedes detener la depuración ahora.

¡Felicidades! Ahora estás listo para añadir más características a la aplicación usando GitHub Copilot.


### 🗒️ (Paso Opcional 2): Familiarízate con los Comandos de Barra de GitHub Copilot

A medida que comenzamos a trabajar en nuestra base de código, generalmente necesitamos refactorizar algún código u obtener más contexto o explicaciones sobre él. Usando el Chat de GitHub Copilot, podemos tener conversaciones orientadas por IA para realizar estas tareas.

Abre el archivo `Program.cs` en el proyecto BackEnd. El archivo está en la siguiente ruta `SampleApp\BackEnd\Program.cs`.

Ahora vamos a usar un comando de barra en GitHub Copilot para entender un fragmento de código. Selecciona las líneas 22-35, presiona `CTRL + I` para abrir el chat en línea y escribe `/explain`.


![Usar comando de barra para explicar un fragmento de código](./011SlashCommandExplain.gif)

En el Panel de Chat, GitHub Copilot creará una explicación detallada del código seleccionado. Una versión resumida sería así:

```
The selected C# code is part of an ASP.NET Core application using the minimal API feature. It defines a GET endpoint at "/weatherforecast" that generates an array of WeatherForecast objects. Each object is created with a date, a random temperature, and a random summary. The endpoint is named "GetWeatherForecast" and has OpenAPI support for standardized API structure documentation.
```
```csharp
El código C# seleccionado forma parte de una aplicación ASP.NET Core que utiliza la característica de API mínima. Define un endpoint GET en "/weatherforecast" que genera un array de objetos WeatherForecast. Cada objeto se crea con una fecha, una temperatura aleatoria y un resumen aleatorio. El endpoint se llama "GetWeatherForecast" y tiene soporte OpenAPI para la documentación estandarizada de la estructura de la API.
```

**Comandos de barra** son comandos especiales que puedes usar en el chat para realizar acciones específicas en tu código. Por ejemplo, puedes usar:
- `/doc` para añadir un comentario de documentación
- `/explain` para explicar el código
- `/fix` para proponer una corrección para los problemas en el código seleccionado
- `/generate` para generar código para responder a tu pregunta

Vamos a usar el comando `/tests` para generar pruebas para el código. Selecciona las líneas 39-42, presiona `CTRL + I` para abrir el chat en línea y escribe `/tests` (o selecciona el comando de barra /tests) para generar un nuevo conjunto de pruebas para este registro.

![Usar comando de barra para generar pruebas para el fragmento de código seleccionado](./012SlashCmdTests.gif)

En este punto, GitHub Copilot sugerirá una nueva clase. Primero debes presionar [Create] para crear el nuevo archivo.

Se ha creado una nueva clase `ProgramTests.cs` y se ha añadido al proyecto. Estas pruebas están usando XUnit, sin embargo, puedes pedir que genere pruebas usando otra biblioteca de pruebas unitarias con un comando como este `/tests use MSTests for unit testing`.

***Importante:** No vamos a usar el archivo de prueba en este proyecto. Debes eliminar el archivo de prueba generado para continuar.*

Finalmente, vamos a usar el `/doc` para generar documentación automática para el código. Selecciona las líneas 39-42, presiona `CTRL + I` para abrir el chat en línea y escribe `/doc` (o selecciona el comando) para generar la documentación para este registro.

![Usar comando de barra para generar la documentación para un fragmento de código](./013SlashCmdDoc.gif)

El chat en línea, el Panel de Chat y los comandos de barra forman parte de las increíbles herramientas que apoyan nuestra experiencia de desarrollo con GitHub Copilot. Ahora estamos listos para añadir nuevas características a esta aplicación.

### 🗒️ Paso 1: Generar un nuevo Registro que incluya el nombre de la ciudad

Ve al archivo `Program.cs` en el proyecto BackEnd. El archivo está en la siguiente ruta `SampleApp\BackEnd\Program.cs`.


![abrir program.cs en el proyecto BackEnd](./011OpenBackEndProject.png)

Navega hasta el final del archivo y pide a Copilot que genere un nuevo registro que incluya el nombre de la ciudad.

```csharp
// create a new internal record named WeatherForecastByCity that request the following parameters: City, Date, TemperatureC, Summary
```

```csharp
// crea un nuevo registro interno llamado WeatherForecastByCity que solicite los siguientes parámetros: City, Date, TemperatureC, Summary
```

El código generado debería ser similar a este:

```csharp
// create a new internal record named WeatherForecastByCity that request the following parameters: City, Date, TemperatureC, Summary
internal record WeatherForecastByCity(string City, DateOnly Date, int TemperatureC, string? Summary)
{
    public int TemperatureF => 32 + (int)(TemperatureC / 0.5556);
}
```
```csharp
// crea un nuevo registro interno llamado WeatherForecastByCity que solicite los siguientes parámetros: City, Date, TemperatureC, Summary
internal record WeatherForecastByCity(string City, DateOnly Date, int TemperatureC, string? Summary)
{
    public int TemperatureF => 32 + (int)(TemperatureC / 0.5556);
}
```

Puedes ver el prompt funcionando en la siguiente animación:

![abrir program.cs en el proyecto BackEnd](./014AddNewRecord.gif)


### 🔎 Paso 2: Generar un nuevo endpoint para obtener la previsión del tiempo para una ciudad

Ahora vamos a generar un nuevo endpoint de API similar a `/weatherforecast` que también incluya el nombre de la ciudad. El nombre del nuevo endpoint de API será **`/weatherforecastbycity`**.

***Importante:** Debes colocar el código después de la línea '.WithOpenApi();', que comienza en la línea 36. Recuerda también presionar TAB en cada nueva línea sugerida hasta que todo el endpoint esté definido.*

A continuación, genera un nuevo endpoint con GitHub Copilot añadiendo el comentario:

```csharp
// Create a new endpoint named /WeatherForecastByCity/{city}, that accepts a city name in the urls as a paremeter and generates a random forecast for that city
```
```csharp
// Crea un nuevo endpoint llamado /WeatherForecastByCity/{city}, que acepte un nombre de ciudad en la URL como parámetro y genere una previsión aleatoria para esa ciudad
```

En el ejemplo siguiente, añadimos algunas líneas en blanco extras después del endpoint anterior y, a continuación, GitHub Copilot generó el nuevo endpoint. Una vez que el código principal del Endpoint fue generado, GitHub Copilot también sugirió código para el nombre del endpoint (línea 49) y la especificación OpenAPI (línea 50). Recuerda aceptar cada una de estas sugerencias presionando [TAB].

![Sugerencia fantasma de Copilot para el nuevo endpoint](./020GeneratedCode.gif)

***Importante**: Este prompt genera varias líneas de código C#. Es altamente recomendable verificar y revisar el código generado para asegurarte de que funcione de la manera deseada.*

El código generado debería ser similar a este:

```csharp
// Create a new endpoint named /WeatherForecastByCity/{city}, that accepts a city name in the urls as a paremeter and generates a random forecast for that city
app.MapGet("/WeatherForecastByCity/{city}", (string city) =>
{
    var forecast = new WeatherForecastByCity
    (
        city,
        DateOnly.FromDateTime(DateTime.Now),
        Random.Shared.Next(-20, 55),
        summaries[Random.Shared.Next(summaries.Length)]
    );
    return forecast;
})
.WithName("GetWeatherForecastByCity")
.WithOpenApi();
```
```csharp
// Crea un nuevo endpoint llamado /WeatherForecastByCity/{city}, que acepte un nombre de ciudad en la URL como parámetro y genere una previsión aleatoria para esa ciudad
app.MapGet("/WeatherForecastByCity/{city}", (string city) =>
{
    var forecast = new WeatherForecastByCity
    (
        city,
        DateOnly.FromDateTime(DateTime.Now),
        Random.Shared.Next(-20, 55),
        summaries[Random.Shared.Next(summaries.Length)]
    );
    return forecast;
})
.WithName("GetWeatherForecastByCity")
.WithOpenApi();
```


### 🐍 Paso 3: Probar el nuevo endpoint

Finalmente, verifica si el nuevo endpoint está funcionando iniciando el proyecto desde el panel Run and Debug. Selecciona Run and Debug y, a continuación, selecciona el proyecto BackEnd.

![Abrir el panel Run and Debug y seleccionar el proyecto BackEnd](./030RunAndDebugTheBackEndProject.png)

Ahora presiona Run y el proyecto debería compilarse y ejecutarse. Una vez que el proyecto esté en ejecución, podemos probar la URL original usando la URL de tu Codespace y el endpoint original:


```bash
https://< tu url de codespace >.app.github.dev/WeatherForecast
```

Y el nuevo endpoint también estará listo para ser probado. Aquí hay algunas URLs de ejemplo con diferentes ciudades:

```bash
https://< tu url de codespace >.app.github.dev/WeatherForecastByCity/Toronto

https://< tu url de codespace >.app.github.dev/WeatherForecastByCity/Madrid

https://< tu url de codespace >.app.github.dev/WeatherForecastByCity/<CualquierNombreDeCiudad>
```

Ambas pruebas en ejecución deberían verse así:

![Abrir el panel Run and Debug y seleccionar el proyecto BackEnd](./032TestAndDebugUsingUrls.png)


🚀 ¡Felicidades, a través del ejercicio, no solo has usado GitHub Copilot para generar código, sino que también lo has hecho de una manera interactiva y divertida! Puedes usar GitHub Copilot no solo para generar código, sino también para escribir documentación, probar tus aplicaciones y mucho más.


## Avisos Legales

Microsoft y cualquier colaborador te otorgan una licencia para la documentación de Microsoft y otros contenidos en este repositorio bajo la [Licencia Pública Internacional Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/legalcode),
ver [LICENSE](LICENSE) y te otorgan una licencia para cualquier código en el repositorio bajo la [Licencia MIT](https://opensource.org/licenses/MIT), consulta
[LICENSE-CODE](LICENSE-CODE)

Microsoft, Windows, Microsoft Azure y/u otros productos y servicios de Microsoft mencionados en la documentación pueden ser marcas comerciales o marcas registradas de Microsoft en los Estados Unidos y/u otros países. Las licencias de este proyecto no te otorgan derechos para usar ningún nombre, logotipo o marca comercial de Microsoft. Las directrices generales de marcas de Microsoft se pueden encontrar en http://go.microsoft.com/fwlink/?LinkID=254653.

La información de privacidad se puede encontrar en https://privacy.microsoft.com/en-us/

Microsoft y cualquier colaborador se reservan todos los demás derechos, ya sea bajo sus respectivos derechos de autor, patentes o marcas comerciales, ya sea por implicación, impedimento legal o de otro modo. 