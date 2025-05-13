<header>

# Creando un Mini Juego con GitHub Copilot

Nuestro enfoque en este módulo es aprovechar el poder de GitHub Copilot para crear un minijuego clásico de piedra, papel o tijera. Esta experiencia práctica no solo mejorará tus habilidades de programación, sino también tu capacidad para desarrollar aplicaciones de consola en Python. ¿La mejor parte? Utilizaremos GitHub Codespaces, eliminando la necesidad de configurar tu entorno de desarrollo. Con GitHub Copilot como tu programador en pareja con IA, puedes concentrarte en el desarrollo de la aplicación mientras colaboras perfectamente con tu asistente de código.

</header>

- **¿Para quién es esto?:** Desarrolladores, Ingenieros DevOps, Gerentes de desarrollo de software, Testers.
- **Lo que aprenderás:** Aprovechar GitHub Copilot para crear código y añadir comentarios a tu trabajo.
- **Lo que construirás:** Archivos Python que tendrán código generado por la IA de Copilot para sugerencias de código y comentarios.
- **Prerrequisitos:** Para usar GitHub Copilot, debes tener una suscripción activa de GitHub Copilot Business o Enterprise. Regístrate para Copilot Free para VS Code solo para fines de entrenamiento [Copilot for free para VS Code](https://learn.microsoft.com/en-us/visualstudio/ide/copilot-free-plan?view=vs-2022).
- **Tiempo:** Este curso puede completarse en menos de una hora.
  
Al final de este módulo, adquirirás las habilidades para:

- Experimentar con GitHub Codespaces como un entorno de desarrollo.
- Desarrollar rutinas de entrada y salida en una aplicación de consola Python.
- Usar GitHub Copilot como asistente.

## Lecturas previas requeridas:
- [Introducción a la ingeniería de prompts con GitHub Copilot](https://learn.microsoft.com/training/modules/introduction-prompt-engineering-with-github-copilot//?WT.mc_id=academic-113596-abartolo)
- [Proyecto de desafío - Construir un minijuego con GitHub Copilot y Python](https://learn.microsoft.com/training/modules/challenge-project-create-mini-game-with-copilot/?WT.mc_id=academic-113596-abartolo)
- Learn Live: Construir una aplicación de consola de minijuego con GitHub Copilot (Video a continuación)
- [![Learn Live: Construir una aplicación de consola de minijuego con GitHub Copilot](https://mediusimg.event.microsoft.com/video-53275/b508053c0b/thumbnail.jpg?sv=2018-03-28&sr=c&sig=k6NthrPwnvBfDPNAEBQaYaVzlJavZ8pnWuP6OcKm4Bs%3D&se=2028-11-18T05%3A23%3A52Z&sp=r)](https://ignite.microsoft.com/sessions/aeaf1e85-65e2-497d-aaf5-724d85213aa1?WT.mc_id=academic-113596-abartolo)
  

## Requisitos

- Habilita tu [servicio GitHub Copilot](https://github.com/github-copilot/signup)

## 💪🏽 Ejercicio

**Haz clic derecho en el botón "Iniciar Curso" para abrir tu Codespace en una nueva pestaña**
 
[![Iniciar Curso](https://user-images.githubusercontent.com/1221423/235727646-4a590299-ffe5-480d-8cd5-8194ea184546.svg)](https://github.com/new?template_owner=skills&template_name=copilot-codespaces-vscode&owner=%40me&name=skills-copilot-codespaces-vscode&description=My+clone+repository&visibility=public)

Ya has aprendido un poco sobre GitHub Codespaces y GitHub Copilot y cómo funcionan. En este ejercicio de desafío, tu objetivo es desarrollar un minijuego en Python usando GitHub Copilot.

#### Probando tu GitHub Codespace

1. Accede a tu Codespaces y crea un nuevo archivo llamado app.py en Visual Studio Code.

    **Nota:** Puede ser necesario instalar la extensión de Python en Visual Studio Code si no está instalada actualmente.

2. Escribe el siguiente comentario:

   ```python
   # write 'hello world' to the console
   ```
      ```python
   # escribe 'hello world' en la consola
   ```
      
3. GitHub Copilot debería completar el código para ti y proporcionar el siguiente resultado:
   
   ```python
   # write 'hello world' to the console
   print('hello world')
   ```
    ```python
   # escribe 'hello world' en la consola
    print('hello world')
   ```

4. Ejecuta la aplicación con el comando python app.py en el terminal y verifica que el resultado sea similar al siguiente mensaje de consola:

   ```bash
   hello world
   ```
   
### Creando la lógica del juego

Ahora que has verificado que Codespaces está funcionando con GitHub Copilot, tu siguiente paso es desarrollar la lógica del minijuego en Python con la ayuda de GitHub Copilot basándote en las siguientes especificaciones:

El ganador del juego se determina por tres reglas simples:

- **Piedra** vence a tijera.
- **Tijera** vence a papel.
- **Papel** vence a piedra.

#### Consideraciones sobre la interacción del juego

La computadora será tu oponente y puede elegir aleatoriamente uno de los elementos (**piedra**, **papel** o **tijera**). Tu interacción con el juego será a través de la consola (Terminal).

- El jugador puede elegir una de las tres opciones: piedra, papel o tijera y debe ser advertido si ingresa una opción inválida.
- En cada ronda, el jugador debe ingresar una de las opciones de la lista y ser informado si ganó, perdió o empató con el oponente.
- Al final de cada ronda, el jugador puede elegir si desea jugar de nuevo.
- Mostrar la puntuación del jugador al final del juego.
- El minijuego debe manejar las entradas del usuario, convirtiéndolas a minúsculas e informando al usuario si la opción es inválida.

En tu GitHub Codespaces, sigue las instrucciones proporcionadas para configurar indicaciones que GitHub Copilot pueda entender y usar para ayudarte a construir el minijuego. Recuerda que GitHub Copilot depende de comentarios para entender el contexto y proporcionar sugerencias útiles mientras trabajas en tu proyecto.

#### Verifica tu trabajo

1. Ejecuta el minijuego en la consola con el comando python app.py.
2. En el prompt, escribe una de las opciones del juego: piedra, papel o tijera.
3. El minijuego debe informar al jugador si ganó, perdió o empató con el oponente.
4. Elige continuar jugando.
5. En el prompt, escribe pantalla.
6. El minijuego debe informar al jugador si la opción ingresada es inválida.
7. Repite los pasos 2 y 4 para jugar algunas rondas y elige no continuar jugando.
8. Verifica que el minijuego se cierre y muestre tu puntuación, informando el número de victorias y rondas.

¡Felicidades por completar este ejercicio de desafío! Has creado un minijuego de consola en Python usando GitHub Copilot.

## Avisos Legales
 
Microsoft y cualquier colaborador te otorgan una licencia para la documentación de Microsoft y otros contenidos en este repositorio bajo la [Licencia Pública Internacional Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0/legalcode),
ver [LICENSE](LICENSE) y te otorgan una licencia para cualquier código en el repositorio bajo la [Licencia MIT](https://opensource.org/licenses/MIT), consulta
[LICENSE-CODE](LICENSE-CODE)
 
Microsoft, Windows, Microsoft Azure y/u otros productos y servicios de Microsoft mencionados en la documentación pueden ser marcas comerciales o marcas registradas de Microsoft en los Estados Unidos y/u otros países. Las licencias de este proyecto no te otorgan derechos para usar ningún nombre, logotipo o marca comercial de Microsoft. Las directrices generales de marcas de Microsoft se pueden encontrar en http://go.microsoft.com/fwlink/?LinkID=254653.
 
La información de privacidad se puede encontrar en https://privacy.microsoft.com/en-us/
 
Microsoft y cualquier colaborador se reservan todos los demás derechos, ya sea bajo sus respectivos derechos de autor, patentes o marcas comerciales, ya sea por implicación, impedimento legal o de otro modo. 