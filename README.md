# Cerebro v0.1

## Introducción

Cerebro es el núcleo de la aplicación de control de flujo y filtrado de mensajes del Proyecto Delta.

## Configuración

Para configurar el flujo y filtrado de mensajes solo tiene que modificar el archivo `app/core/config.py`, en él se encuentra un diccionario llamado `_config` con la siguiente estructura:

```python
_config = {
    'etiqueta_del_modulo': {
        'url': 'http://www.example.com/',
        'tags': ['tag1', 'tag2'],
        'transitions': [
            {
                'query': lambda tags: True,
                'next_module': 'etiqueta_siquiente_modulo'
            }, {...}
        ]
    }, {...}
}
```

Luego de editado el diccionario guarde el archivo y listo, ya puede iniciar el servidor.

## Notas de la versión

Esta versión esta basada en hilos o threads utilizando los módulos dummy_threading.threading y threading.
