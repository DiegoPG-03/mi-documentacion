# Configuración del Entorno

Una vez instaladas las herramientas base, es necesario realizar algunas configuraciones adicionales para optimizar nuestro flujo de trabajo.

## Variables de Entorno
En sistemas Windows, es recomendable configurar la variable de entorno `JAVA_HOME`.
1. Abre las propiedades del sistema y dirígete a "Variables de entorno".
2. Crea una nueva variable de sistema llamada `JAVA_HOME` apuntando al directorio donde instalaste el JDK.
3. Edita la variable `Path` y añade la ruta `%JAVA_HOME%\bin`.

## Configuración de Apache NetBeans
1. Abre Apache NetBeans.
2. Ve a **Tools > Options**.
3. En la pestaña de **Java**, verifica que la ruta del JDK sea reconocida correctamente por el programa.
4. Puedes ajustar el tema visual y el tamaño de la fuente en la sección de **Appearance** para mayor comodidad.