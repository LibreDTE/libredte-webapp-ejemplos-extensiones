Extensión: e004_modulo
==========================

Esta extensión requiere modificar la configuración en Config/core.php


    // Módulos que utiliza la aplicación
    \sowerphp\core\Module::uses([
        // módulos estándares (disponibles para todas las empresas)
        'Dte',
        // ... otros módulos
        'MiModulo', // módulo que se creó en la extensión
    ]);

Cambios
-------

- Agrega un nuevo módulo y controlador con una acción a la app disponible en example.com/mi\_modulo/controlador/accion_x
