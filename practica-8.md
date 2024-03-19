# Práctica 8 - Preguntas

1.  **¿Cómo se inicializa un repositorio en _Git_?**

  Una vez que tengamos la carpeta de nuestro proyecto abierta en _Visual Studio_, deberemos de escribir el siguiente comando en la terminal:

  ```bash
  git init 
  ```

2.  **¿Cómo creas un repositorio en _GitHub_?**

  Para crear un repositorio en _GitHub_, deberemos de presionar el botón de "+" en la parte superior derecha de la pantalla en el menú principal de _GitHub_. Este botón nos servirá para crear un nuevo repositorio. Tendremos que ponerle un nombre, una url personalizada y elegir la configuración que deseemos.

3. **¿Cómo vinculas un repositorio local de _Git_ con uno remoto en _GitHub_?**

  Para vincular nuestro repositorio local con el remoto, primero deberemos agregar el origen remoto. Una vez que hayamos creado nuestro repositorio en GitHub, copiaremos la url y la reemplazaremos en la siguiente línea de código:

 ```bash
 git remote add origin https://github.com/usuario/repositorio.git
 ```

 Posteriormente, para actualizar los cambios que hayamos realizado, deberemos utilizar la siguiente línea de código:

  ```bash
 git push -u origin
 ```

 Esto solo será necesario la primera vez, los cambios posteriores los podremos actualizar con el comando:

   ```bash
 git push 
 ```

4.  **¿Cuál es el flujo básico de trabajo en _Git_ y _GitHub_?**

El flujo básico de trabajo es básicamente el recorrido que toman las actualizaciones que hagamos en nuestro proyecto. Es llevar de el punto _A_ (repositorio local) al punto _B_ (repositorio remoto) los cambios que realizemos, pasando por diferentes etapas o estados. Dichos estados son: 

  - _modified_: Archivos modificados en el repositorio local.

  - _staged_: Los cambios en los archivos antes de ser comprometidos al registro.

  - _comitted_: Registro de los cambios realizados.

  - _remote_: Archivos modificados y actualizados en el repositorio remoto.

![Flujo básico Git](https://jonmircha.com/img/blog/git-flow.png)

5. **¿Para qué sirve el archivo _.gitignore_?**

  Podemos agregar un archivo _.gitignore_ a nuestro proyecto para bloquear o ignorar cierto tipo de archivos que no querramos en nuestro repositorio. Podemos bloquear archivos por extensión y también hacer excepciones. Por ejemplo, si queremos bloquear los ejecutables, dentro del archivo _.gitignore_ escribiremos lo siguiente:

```bash
* .exe
 ```

 Y si queremos hacer alguna excepción:

```bash
# ignoramos los archivos con extensión exe
* .exe
# exceptuando el archivo EjecutablePermitido
!EjecutablePermitido.exe
 ```

6. **¿Cuál es el propósito de una rama?**

  Las ramas nos permiten trabajar sobre un mismo proyecto desde diferentes puntos. Esto nos sirve para trabajar en equipo de manera más organizada, ya que, cada miembro del equipo puede crear su propia rama del proyecto para comenzar a realizar todos sus cambios ahí y una vez que termine, actualizar dichos cambios fusionando su rama con la rama principal del proyecto.

7.  **¿Qué es una fusión?**

  La fusión es cuando se unen 2 ramas. Por ejemplo, cuando un integrante del equipo ha terminado de realizar sus cambios y quiere actualizarlos al proyecto original, deberá fusionar la rama donde realizo los cambios con la rama principal. De esta manera, todos los integrantes del equipo podrán visualizar dichos cambios en el repositorio remoto.

8. **Explica los diferentes tipos de fusión que existen.**

  Existen 2 tipos: _Fast-forward_ y _Manual_.

  - **_Fast-forward_ merge**: Es cuando la fusión se hace de manera automática, debido a que no hay ningún conflicto.

  - **_Manual_ merge**: Es cuando debemos de hacer modificaciones manualmente para que se puedan fusionar las ramas. Esto ocurre cuando hay algún conflicto, como archivos duplicados, por lo que tenemos que indicarle al programa de qué manera resolver dichos conflictos.

9.  **¿Cómo puedes ver el historial de tu repositorio?**

En la terminal de comandos, podemos observar el historial con el siguiente comando:

```bash
git log

#mismo comando, pero nos muestra un cambio por línea
git log --oneline
 ```

También podemos crear un archivo que contenga el historial con el siguiente comando:

```bash
git log > commits.txt
 ```

Y también podemos ver el historial desde _GitHub_, con el botón de _Commits_, el cual tiene un símbolo como de un reloj y podemos encontrar en la página principal de nuestro repositorio.

10. **¿Cuál es el propósito de una etiqueta?**

Nos permite crear diferentes versiones de nuestro proyecto.

