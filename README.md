# Una casa inteligente con Home Assistant · Repositorio del libro

Códigos y prompts del libro *Una casa inteligente con Home Assistant*, de David Vicioso Adrià.
Libro independiente, no afiliado al proyecto Home Assistant ni a la Open Home Foundation.

## El libro

📖 **[Una casa inteligente con Home Assistant](https://amzn.eu/d/0gwAR9Nm)**, en Amazon, en papel y en versión electrónica.

Este repositorio reúne los códigos del libro para que no tengas que copiarlos a mano. El libro explica paso a paso qué hace cada uno, cómo adaptarlo a tu casa y qué errores evitar.

## Qué hay aquí

| Carpeta | Contenido | Capítulo |
|---|---|---|
| `prompts/` | El prompt inicial del proyecto, completo | Anexo A |
| `automatizaciones/` | Las automatizaciones del libro, en YAML y comentadas | 10, 11 y 12 |
| `automatizaciones/mi-casa/` | Las versiones ampliadas que uso en mi casa: avisos de humo y agua insistentes a dos móviles, y la rutina de buenos días con reintentos | 12 |
| `scripts/` | Rutinas de un toque | 12 |
| `paneles/` | Los paneles HTML de la tablet y del móvil | 9 |
| `instalacion/` | Arranque automático de la máquina virtual en Windows | 5 |

Cada archivo indica al principio si es código **comprobado** en la casa del autor, **en uso pendiente de probar** o un **ejemplo ilustrativo** del libro.

Empieza por los archivos de `automatizaciones/`, que son los que explica el libro paso a paso. Los de `mi-casa/` añaden técnicas más avanzadas (repeticiones, avisos críticos, varios móviles); úsalos cuando entiendas los básicos.

## Antes de usar nada

1. **Cambia los identificadores.** Todos los `entity_id` (`light.luz_comedor`, `climate.calefactor_bano`…) son de ejemplo. Los tuyos están en *Configuración → Herramientas para desarrolladores*, pestaña *Estados* (capítulo 15).
2. **Haz una copia de seguridad** antes de pegar código (capítulo 14).
3. **Entiende lo que pegas.** Si no sabrías explicarlo con una frase, no lo pegues todavía (capítulo 11).
4. **Nunca publiques ni compartas** contraseñas, claves de acceso ni tu archivo `secrets.yaml`.

## Cómo usar los paneles

1. Abre el archivo y edita el bloque `CONFIGURACIÓN` del principio con tus entidades.
2. Guárdalo en la carpeta `www` de tu configuración de Home Assistant (por ejemplo, `www/panel/panel-tablet.html`).
3. Ábrelo en `http://homeassistant.local:8123/local/panel/panel-tablet.html`. La página usa la sesión de Home Assistant iniciada en ese navegador: si no la hay, te pedirá entrar.
4. Si cambias el archivo y no ves el cambio, añade `?v=2`, `?v=3`… al final de la dirección (apartado 9.4).

Los datos de facturas y consumos de los paneles son **inventados**. Bórralos o sustitúyelos por los tuyos.

Todos los identificadores, nombres de personas y datos de este repositorio son de ejemplo: he quitado los míos por seguridad.

## Licencia

Código bajo licencia MIT: puedes usarlo y modificarlo libremente, sin garantía de ningún tipo.
