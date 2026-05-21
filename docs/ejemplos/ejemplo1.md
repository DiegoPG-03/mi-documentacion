# Ejemplo 1: Conexión y Consulta a MySQL

A continuación, se muestra un ejemplo básico de cómo establecer una conexión a una base de datos MySQL y realizar una consulta relacionando dos tablas utilizando Java (JDBC).

## Código Fuente

```java
import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.ResultSet;
import java.sql.Statement;

public class ConexionBBDD {
    public static void main(String[] args) {
        String url = "jdbc:mysql://localhost:3306/instituto";
        String usuario = "root";
        String contrasena = "123456";

        try {
            // Establecer conexión
            Connection conexion = DriverManager.getConnection(url, usuario, contrasena);
            System.out.println("¡Conexión establecida!");

            // Realizar consulta
            Statement stmt = conexion.createStatement();
            String query = "SELECT a.nombre, c.nombre_curso FROM alumnos a JOIN cursos c ON a.id_curso = c.id_curso";
            ResultSet rs = stmt.executeQuery(query);

            while (rs.next()) {
                System.out.println("Alumno: " + rs.getString("nombre") + " - Curso: " + rs.getString("nombre_curso"));
            }

            conexion.close();
        } catch (Exception e) {
            System.out.println("Error en la base de datos.");
            e.printStackTrace();
        }
    }
}