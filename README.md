LibreDTE: ejemplos de extensiones para libredte-webapp
======================================================

En este repositorio encontrarás ejemplos básicos de extensiones que se pueden
crear para personalizar la aplicación web de LibreDTE.

Es deber del programador unir estos ejemplos según sus requerimientos. Lo
correcto es crear sólo una extensión que tenga todo el código que modifica la
aplicación web de LibreDTE, y no cargar cada extensión por separado. Están por
separado sólo por orden y simplicidad para mostrar cómo se construye cada caso.

Adicionalmente el programador, deberá completar/mejorar el código de cada
extensión. Estas, no serán, necesariamente, ejemplos funcionales. Se deberán en
la mayoría de los casos modificar para lograr la funcionalidad real esperada.
Se pueden buscar los **TODO** para saber donde se espera que el programador
realice cambios, pero obviamente podrían ser en cualquier lado, ya que estos
son sólo ejemplos.

¿Cómo creo una extensión en mi instancia web de LibreDTE?
-----------------------------------------------------------------------------

1. Crea el directorio **extensions/vendor/libredte** que será el directorio
   principal de la extensión. **vendor** cámbialo por el nombre de la
   empresa que está proporcionando la instancia de LibreDTE o bien de quien
   desarrollo la extensión.

        $ mkdir extensions/vendor/libredte

    Es importante que asignes un valor de **vendor**, ya que es el que se usará
    en los namespaces de la extensión.

2. Edita **website/webroot/index.php** para especificar las extensiones que
   deseas usar. Debe quedar así (el orden es importante):

        ```php
        $_EXTENSIONS = ['vendor/libredte', 'website', 'sowerphp/app', 'sowerphp/general'];
        ```

    Recuerda colocar **website** o tu aplicación dejará de funcionar.

3. Quita el archivo **website/webroot/index.php** del rastreo de git, ya que lo
   modificaste.

        $ git update-index --skip-worktree website/webroot/index.php

4. Si crearás comandos de **Shell** en tu extensión, repite los pasos 2 y 3 con
   el archivo **website/Shell/shell.php**

5. ¡Listo! Tu extensión está creada y habilitada en la aplicación. Ahora a programar :-)
