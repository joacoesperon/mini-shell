# Sistema de Ficheros Virtual en C

Este proyecto implementa un sistema de ficheros virtual en C que simula operaciones básicas de shell como crear directorios, escribir archivos, listar contenidos, etc.

## Autores

- Marc Nadal Sastre Gondar
- Joaquín Esperon Solari  
- Martí Vich Gispert

## Descripción

El proyecto implementa un sistema de ficheros virtual con funcionalidades similares a las de un shell Unix/Linux. Permite gestionar archivos y directorios en un dispositivo virtual, ofreciendo operaciones básicas como:

- Crear directorios y archivos
- Escribir y leer contenido
- Listar contenidos de directorios
- Modificar permisos
- Eliminar archivos y directorios
- Obtener información de archivos/directorios

## Comandos Implementados

- `mi_mkdir`: Crea un nuevo directorio
- `mi_touch`: Crea un nuevo archivo
- `mi_ls`: Lista el contenido de un directorio (implementado con formato detallado similar a ls -l)
- `mi_cat`: Muestra el contenido de un archivo
- `mi_chmod`: Modifica los permisos de un archivo o directorio
- `mi_stat`: Muestra información detallada de un archivo o directorio
- `mi_rm`: Elimina un archivo
- `mi_rmdir`: Elimina un directorio
- `mi_rm_r`: Elimina recursivamente directorios y su contenido

## Estructura del Sistema de Ficheros

El sistema de ficheros está organizado en:

- Superbloque
- Mapa de bits
- Array de inodos
- Bloques de datos

## Características Técnicas

- Tamaño de bloque: 1024 bytes
- Sistema de permisos similar a Unix (lectura, escritura, ejecución)
- Gestión de metadatos (fechas de creación, modificación, acceso)
- Soporte para enlaces
- Implementación de semáforos para control de concurrencia

## Compilación y Uso

1. Compilar el proyecto:

make

2. Crear y montar el sistema de ficheros:

./mi_mkfs <nombre_dispositivo> <tamaño>

3. Ejemplos de uso:

./mi_mkdir <nombre_dispositivo> <permisos> <ruta>
./mi_ls <nombre_dispositivo> <ruta>
./mi_touch <nombre_dispositivo> <permisos> <ruta>
./mi_cat <nombre_dispositivo> <ruta>

## Notas Adicionales

- El comando `mi_ls` siempre muestra información detallada (similar a ls -l)
- El sistema implementa control de errores y mensajes informativos
- Se utiliza un sistema de colores en la salida para mejor visualización
- Incluye protección contra errores comunes y validación de argumentos

## Limitaciones

- No se ha implementado el comando `mi_touch` de forma independiente (se usa `mi_mkdir` en su lugar)
- Algunas funcionalidades avanzadas de sistemas de ficheros no están implementadas

## Requisitos

- Compilador de C
- Sistema operativo Unix/Linux
- Make

## Licencia

Este proyecto es de uso educativo y está disponible para su estudio y modificación.