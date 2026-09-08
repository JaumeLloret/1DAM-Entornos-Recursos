# Hoja de comandos E1

Permitida en V1–V4. No contiene diagnósticos ni soluciones de los casos. Ejecuta desde la raíz del starter, salvo cuando se pida identificar otra carpeta.

```text
java --version
javac --version
jar --version
mvn --version
mvn validate
mvn clean compile
mvn package
java -cp target/classes aula.e1.Main
java -cp target/e1-entorno-1.0.0.jar aula.e1.Main
jar --list --file target/e1-entorno-1.0.0.jar
jar --create --file target/e1-con-entrada.jar --main-class aula.e1.Main -C target/classes .
java -jar target/e1-con-entrada.jar
```

`pwd`: carpeta actual. `cd "ruta"`: cambiar de carpeta. `java -cp CARPETA_O_JAR CLASE`: los nombres en mayúsculas son marcadores que debes sustituir; no una orden para copiar literalmente.

| Acción | Windows PowerShell | Linux/macOS |
|---|---|---|
| Localizar Java | `Get-Command java,javac` | `command -v java` y `command -v javac` |
| Ver versión C | `gcc --version` | Linux `gcc --version`; macOS `clang --version` |
| Hash de fuente | `Get-FileHash src/main/java/aula/e1/Main.java -Algorithm SHA256` | Linux `sha256sum src/main/java/aula/e1/Main.java`; macOS `shasum -a 256 src/main/java/aula/e1/Main.java` |

Acciones del entorno: Open Folder; Project Structure / SDK; Maven / Runner; Maven / Lifecycle; Terminal / Run Task; Extensions / Install from VSIX; Installed / Uninstall; Settings / Updates; Help / About. Usa búsqueda de acciones si cambia la ubicación.

Tareas suministradas: E1 Java: compilar; E1 Java: empaquetar; E1 Java: ejecutar; E1 C: objeto; E1 C: compilar; E1 C: ejecutar.
