# Nombre del proyecto
SubaWatts
## Descripción
Aplicación desarrollada durante el Técnico en Programación de Software.

## Objetivo
Este proyecto tiene como objetivo identificar y conocer los diferentes Pokemones que existen y/o existieron dentro de la serie animada Pokemon, dentro de la busqueda se pueden observar datos como el nivel de ataque de los pokemones, su nombre, su niver de defensa entre otras...

## Tecnologías
- HTML
- CSS
- JavaScript
- PHP
- API REST / API externa
- Git
- GitHub

## Funcionalidades
- Consultar información
- Mostrar resultados
- Validar datos
- Manejar errores

## Estructura:
1. En el Documento de Agregar:
Este script en PHP procesa la adición de un Pokémon al equipo activo almacenado en la sesión.
Inicia la sesión de PHP y extrae de forma segura los datos enviados por método POST (`id`, `nombre` e `imagen`), asegurando que el identificador sea un número entero y que el nombre no esté vacío. Si los datos no son válidos, interrumpe la ejecución con un mensaje de error.
Recupera el equipo actual de la sesión y verifica que no se supere el límite máximo de 6 miembros permitidos.
Valida mediante un recorrido que el Pokémon que se intenta agregar no forme ya parte del equipo.
Si pasa todas las validaciones, agrega el nuevo Pokémon con sus atributos al arreglo del equipo en la sesión y redirige al usuario a la vista 

2. En el Documento de eliminar.php:
 Inicia la sesión y recupera mediante el método POST el identificador (id) del Pokémon que se desea remover, convirtiéndolo a un número entero.  
 Comprueba si la variable de sesión del equipo existe; si no ha sido inicializada, la define como un arreglo vacío. 
 Recorre los miembros actuales del equipo guardados en la sesión y reconstruye un nuevo arreglo ($nuevoEquipo) omitiendo al Pokémon cuyo id coincida con el recibido por POST (es decir, conservando únicamente a los que tienen un id diferente).  
 Reemplaza el equipo anterior en la sesión con el nuevo arreglo filtrado y redirige al usuario de vuelta a la vista

 3. En el Documento de equipo.php:
 Vista principal que muestra el equipo Pokémon guardado en la sesión (hasta un máximo de 6), indicando el conteo actual de miembros, un enlace para buscar más Pokémon y un botón individual para quitar a cualquier integrante.

 4. En el Documento de estilos.css:
 Hoja de estilos global basada en un diseño estructurado y minimalista, que incluye reglas de reseteo, tipografía centrada para tarjetas de contenido, cuadrículas flexibles para el equipo y la personalización del color de fondo del cuerpo (#5BC2A0).

 5. En el Documento funciones.php:
 Archivo de funciones lógicas y de utilidad. Contiene consultarPokemon($busqueda), encargada de conectar de manera segura con la API externa mediante file_get_contents y decodificar el JSON resultante, además de nombreBonito($texto), que formatea las cadenas reemplazando guiones y capitalizando las palabras.

 6. En el Documento de index.php:
 Pantalla de inicio de la aplicación generada mediante PHP. Renderiza el formulario de búsqueda principal que recopila el nombre o ID del Pokémon y lo envía por método GET hacia pokemon.php.

 7. En el Documento de  Pokemon.php:
 Vista de resultados detallados. Valida la entrada de búsqueda, realiza la consulta a la API, procesa la imagen oficial del sprite e imprime la información biométrica (altura y peso convertidos a unidades métricas), tipos, habilidades y estadísticas base, junto a un formulario para agregar al ejemplar al equipo activo.

## Ejecución
1. Clonar el repositorio.
2. Abrirlo en Visual Studio Code.
3. Si usa PHP, ubicarlo en htdocs o equivalente.
4. Iniciar Apache.
5. Abrir la aplicación desde localhost.

## Autor
Luis Miguel Laverde Farieta
Santiago Perez Watts        
Ficha 3538620
Técnico en Programación de Software - SENA
