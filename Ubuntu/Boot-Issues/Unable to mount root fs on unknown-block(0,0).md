# Kernel Panic
**Kernel Panic/Unable to mount root fs on unknown-block(0,0)**

# Recuperación de Kernel Panic en Azure VM

## Paso 1: Utilizar la Consola de Serie de Azure

Para interactuar con la VM incluso si el sistema operativo no arranca correctamente:

1. **Accede a la Consola de Serie**:
   - En el portal de Azure, ve a la VM que está teniendo problemas.
   - En el panel de la izquierda, selecciona "Conectar" y luego "Consola Serie" bajo las opciones de conexión.

## Paso 2: Revisar y Modificar Configuraciones del GRUB

1. **Modificar Configuraciones Temporales**:
   - Reinicia la VM y durante el arranque, intenta entrar al menú de GRUB presionando `Esc` o `Shift`.
   - Modifica las opciones de arranque, ajustando la configuración de `root=` para apuntar a la partición correcta.

## Paso 3: Modo de Recuperación

1. **Usar el Modo de Recuperación**:
   - Desde el GRUB, selecciona una opción de "recovery mode" para acceder a un entorno más estable.

2. **Verificar y Reparar el Sistema de Archivos**:
   - Desde el modo de recuperación, usa el comando `fsck` para verificar y reparar la partición de sistema de archivos raíz.

## Paso 4: Revisar la Configuración de los Discos

1. **Revisar Configuración de Almacenamiento en Azure**:
   - Asegúrate de que la configuración de discos y almacenamiento en Azure esté correcta y que la VM esté apuntando a los discos adecuados.

## Paso 6: Contactar Soporte de Azure

Si todos estos pasos fallan, considera contactar al soporte de Azure para obtener ayuda adicional.
