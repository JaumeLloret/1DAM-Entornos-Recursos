# Starter técnico E1

Proyecto de práctica creado para E1; no es el código de AulaFlow ni su arquitectura.

Requisitos: JDK 26 (referencia Temurin 26.0.2), Maven 3.9.16. No necesita cuentas, base de datos, servidor ni librerías de aplicación externas. La primera construcción Maven necesita conexión para descargar sus herramientas.

## Ruta principal: IntelliJ IDEA gratuito equivalente a Community

Abre esta carpeta o su `pom.xml` como proyecto. Selecciona JDK 26 para proyecto y Maven. Sigue el ejemplo G03 de la unidad. Desde una terminal situada en esta carpeta:

```text
java --version
javac --version
mvn --version
mvn clean compile
java -cp target/classes aula.e1.Main
mvn package
java -cp target/e1-entorno-1.0.0.jar aula.e1.Main
```

Las dos primeras líneas de la aplicación deben ser:

```text
E1 | entorno preparado
Especificacion Java: 26
```

La tercera informa del parche real. Este JAR Maven no declara `Main-Class`; se ejecuta con `-cp` y el nombre de la clase. No se promete que funcione con doble clic ni con `java -jar`.

## Comparación acotada: VSCodium

Abre la misma carpeta. Abre Terminal → Run Task y elige `E1 Java: ejecutar`. La tarea compila, genera otro JAR con punto de entrada y lo ejecuta. El código fuente no cambia. Se usa la integración de tareas, no se exige un complemento Java ni se evalúa editar JSON.

Para RA2.e, instala el compilador C indicado en G07 y ejecuta `E1 C: ejecutar` desde el mismo VSCodium. Salida: `E1 | salida nativa`. C es una muestra suministrada, no contenido de programación de E1. `E1 C: objeto` permite observar un `.o` sin enlazar.

## Archivos que se conservan

Conserva `pom.xml`, `src/`, `comparacion/`, `.vscode/tasks.json` y este README. `target/`, `salida-java/`, `salida-c`, `salida-c.exe` y `saludo.o` son productos regenerables. No entregues instaladores ni cachés.

## Fallos para practicar

Realiza los fallos F01–F06 del laboratorio únicamente sobre una copia. No cambies la versión 26 del POM para eludir un error. No borres tu JDK ni modifiques permisos de seguridad globales.

## Alcance de reproducibilidad

Se exige reconstruir y ejecutar con las mismas fuentes, versión de Java y configuración. No se exige igualdad binaria de los JAR ni de ejecutables nativos entre sistemas operativos. Consulta la auditoría docente para el estado de validación.
