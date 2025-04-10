# Equipo18-ManejoDatos
# Manejador de Archivos (.txt, .csv, .json)

**Equipo 18**  
**Integrantes:**
- Sandoval Reyes Miguel  
- García Pérez César Miguel

## Descripción del Proyecto

ManejadorArchivos es una librería en Java orientada al manejo eficiente de archivos en formato TXT, CSV y JSON. Permite leer, escribir y convertir datos entre estos formatos de manera sencilla, utilizando métodos estáticos sin necesidad de dependencias externas.

## Funcionalidades principales

- **Exportación:** Guarda el contenido escrito en un `JTextArea` en formato `.txt`, `.csv` o `.json`.
- **Conversión:** Convierte archivos entre los formatos `.txt`, `.csv` y `.json`.
- **Validaciones:** La aplicación valida rutas vacías, extensiones repetidas, errores de lectura/escritura, y más.

## Estructura del proyecto

El proyecto se compone de dos clases principales:

- **ManejadorArchivos**: Funcionalidad para manipular archivos y convertir formatos.
- **Registro**: Representación de un registro de datos genérico utilizado para almacenamiento o visualización.

## Clases y métodos

### ManejadorArchivos.java

Clase estática con funciones para manejo de archivos.

#### Descripción general

La clase ManejadorArchivos implementa métodos estáticos para:

- Leer y escribir archivos de texto plano.
- Leer y escribir archivos CSV y JSON.
- Convertir entre formatos CSV, JSON y TXT.
- Parsear estructuras JSON simples sin bibliotecas externas.
- Validar rutas vacías, extensiones repetidas, errores de lectura/escritura, y más.

#### Lectura y escritura de texto

```bash
public static String leerArchivoTexto(String ruta)
```
// Lee el contenido completo de un archivo .txt.
```bash
public static void escribirArchivoTexto(String ruta, String contenido)
```
// Sobrescribe el contenido de un archivo .txt.
```bash
public static void agregarTextoArchivo(String ruta, String contenido)
```
// Agrega contenido al final de un archivo de texto.

### Manejo de CSV
```bash
public static List<String[]> leerArchivoCSV(String ruta)
```
// Lee un archivo .csv línea por línea, devolviendo una lista de arreglos de cadenas.
```bash
public static void escribirArchivoCSV(String ruta, List<String[]> datos)
```
// Escribe una lista de datos en un archivo .csv.
```bash
public static List<Map<String, String>> leerArchivoCSVConCabeceras(String ruta)
```
// Lee un .csv con cabeceras, devolviendo una lista de mapas (clave = cabecera, valor = celda).

### Manejo de JSON
```bash
public static Map<String, Object> leerArchivoJSON(String ruta)
```
// Lee un archivo .json y lo transforma en un Map.
```bash
public static void escribirArchivoJSON(String ruta, Map<String, Object> datos)
```
// Escribe un Map como archivo .json.
```bash
public static Map<String, Object> parsearJSON(String json)
```
// Parsea manualmente una cadena JSON en un Map.
```bash
public static String convertirJSON(Map<String, Object> datos)
```
// Convierte un Map en una cadena JSON.
****
###Conversión entre formatos
