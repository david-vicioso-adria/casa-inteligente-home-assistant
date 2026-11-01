# Arranque automático de la máquina virtual en Windows (apartado 5.D)

Estado: COMPROBADO en la casa del autor.

1. Abre el **Programador de tareas** de Windows y crea una tarea básica que se ejecute **al iniciar sesión**.
2. Acción: iniciar un programa.
   - Programa: `C:\Program Files\Oracle\VirtualBox\VBoxManage.exe` (comprueba la ruta en tu equipo).
   - Argumentos: `startvm "Home Assistant" --type headless`
3. Guarda la tarea y reinicia el ordenador para comprobarlo.

`"Home Assistant"` es el nombre de la máquina virtual en VirtualBox: si la llamaste de otra forma, cámbialo.
`--type headless` la arranca sin ventana, en segundo plano.

Recuerda configurar Windows para que no se suspenda ni hiberne (ni al cerrar la tapa, si es un portátil).

## Importante: la tarea necesita que alguien inicie sesión

Con el desencadenador **al iniciar sesión**, si Windows se reinicia solo (por ejemplo, tras una actualización) y se queda en la pantalla de acceso, la máquina virtual no arranca hasta que alguien entra. Dos formas de evitarlo:

- **Inicio de sesión automático en Windows.** Cómodo, pero deja el ordenador abierto a quien lo encienda.
- **Desencadenador «al iniciar el equipo»** y, en las propiedades de la tarea, la opción de ejecutarla aunque el usuario no haya iniciado sesión. Pega: la máquina virtual arranca en una sesión aparte y no aparece «en ejecución» en la ventana de VirtualBox, aunque funcione.

Elijas la que elijas, reinicia el ordenador y comprueba que Home Assistant responde sin tocar nada.
