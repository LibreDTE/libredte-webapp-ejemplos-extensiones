Extensión: e003_triggers
==========================

Esta extensión requiere modificar la configuración en Config/core.php

    // handler para triggers de la app
    \sowerphp\core\Configure::write('app.trigger_handler', '\libredte\e003_triggers\Trigger_Handler::run');

En general los triggers no retornan datos, pero podría ser necesario, revisar
los que tienen retornos asignados para saber cuales se espera retornen algo.

Si se desea generar un error dentro de un trigger, se debe lanzar una excepción:

    throw new \Exception('Error dentro del trigger');

Cambios
-------

- Se agrega handler para los triggers de la aplicación.
