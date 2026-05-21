# Despliegue y Ejecución

A diferencia de las aplicaciones web, los proyectos estándar en Java se compilan y empaquetan de una forma específica para su posterior distribución.

## Compilación del Proyecto
Apache NetBeans facilita este proceso mediante su sistema de construcción.
- Para compilar el proyecto, simplemente haz clic en el botón **"Build Project"** (icono del martillo) en el menú superior o presiona `F11`.
- Esto generará los archivos `.class` a partir de tu código fuente y creará un archivo `.jar` ejecutable en la carpeta `dist/` de tu proyecto.

## Ejecución
- Puedes probar el código directamente desde el IDE pulsando el botón **"Run Project"** (icono de play verde) o con la tecla `F6`.
- Para desplegar y ejecutar el archivo `.jar` compilado desde la consola, utiliza el siguiente comando:
  ```bash
  java -jar dist/NombreDelProyecto.jar
