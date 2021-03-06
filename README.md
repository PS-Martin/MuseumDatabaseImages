# MuseumDatabaseImages
Macro to organize and maniulate pictures and links to files inside a museum database. The instructions are in Spanish: contact me for further info or a request of a translation.

::::::::::::::::::::::::::::
INSTRUCCIONES PARA EL USO DEL PROGRAMA DE ACTUALIZACIÓN DE ICONOS DEL INVENTARIO DEL MUSEO
::::::::::::::::::::::::::::

	Este programa está diseñado para funcionar aplicado a la base de datos del inventario de la biblioteca de la ETSIT-UPM. Para ejecutarse en otros excels requeriría adaptar el código.

	Este programa permite actualizar automáticamente hasta 50 elementos en la columna de imagen en el libro IDENTIFICACIÓN del inventario. Es decir, cuando se ejecuta, para los elementos seleccionados se adjunta una imagen a modo de icono que se ajusta a la celda asignada a su número de inventario, y esta imagen se combina con un hipervínculo que enlaza con las imágenes de la base de datos, para que al hacer click puedan visualizarse a mayor tamaño desde la propia colección de imágenes.
	Para activarlo debe hacerse click sobre el botón “Actualizar”:
 
Tras ello aparecerá un cuadro en el que podremos seleccionar el rango de elementos (según el número de inventario):
 
En este cuadro se ha de indicar el número de registro de la pieza desde la cual queremos actualizar, y el número de registra de la pieza hasta la cual queremos actualizar. El número de registro de cada pieza puede escribirse estrictamente según el formato del registro (por ejemplo 00.992), o bien indicando el número sin más (992).
Una vez seleccionado el rango, se hace click en el botón “Iniciar”, y el proceso se realizará en unos segundos sin requerir más acciones. Puede repetirse tantas veces como se quiera, ya que las imágenes en el rango seleccionado se borrarán y añadirán de nuevo cada vez que se active el programa.

LIMITACIONES DEL PROGRAMA

—El programa no nos permite actualizar más de 50 elementos por vez, acción que nos devolvería una advertencia.
—El programa sólo funciona hasta el número de registro 10.000, no incluido. Para funcionar con un catálogo de 10.000 piezas debería modificarse el código.
—El programa sólo admite hasta 8 elementos secundarios por pieza. (a,b,c,d,e,f,g,h). Si una pieza contara con más elementos el programa no los incluiría y podría numerar mal las imágenes a partir del último elemento. En este caso se recomienda actualizar esa pieza por separado, y no incluirla entre el rango seleccionado.
—No se pueden actualizar elementos desde un accesorio. Es decir: en los cuadros de número inicial y final deben de figurar únicamente números de registro principales (sin letras).

ADVERTENCIA PARA EL CORRECTO FUNCIONAMIENTO DEL PROGRAMA Y TRATAMIENTO DE ERRORES:

Aunque se ha tratado de cubrir todos los errores y posibles usos incorrectos del programa, es necesario tener en cuenta algunas cosas, pues de lo contrario el programa podría fallar. Ante un fallo del programa, podría devolver un mensaje como este (con cualquier número de error):
 
Si no se tienen conocimientos adecuados en programación debe hacerse click en “Finalizar”, que detendrá todo el programa sin mayor problema. Nunca en “Depurar”, que abriría el código del programa y cualquier cambio sin conocimiento en la materia puede dañar el programa.

Ante este tipo de errores, o si el programa no realizara las acciones solicitadas sin informar de error, debe comprobarse que se cumplen las siguientes condiciones, pues normalmente una de ellas no se cumplirá:

—Los números de registro están perfectamente escritos en su columna, siguiendo el formato establecido (ej: 00.013). No puede haber espacios ni ningún símbolo extraño. Para detectar espacios añadidos a veces a continuación, dado que son invisibles, podemos fijarnos en cuál es la última pieza que se ha actualizado correctamente tras ejecutar el programa. Normalmente la siguiente en la lista tendrá el espacio buscado, que deberemos eliminar.

—El archivo Excel del inventario está en la carpeta adecuada dentro de H:\MUSEO

—Las imágenes existen en cada carpeta (carpetas: 2_Retocadas y 4_Iconos) Y han sido nombradas correctamente siguiendo las mismas pautas que todas las demás (ej: MUSEO 00991_1.jpg)

—No hay números de registro en blanco en el libro Excel de identificación a lo largo del rango dado: es decir, si se actualizan por ejemplo las 50 primeras piezas, debe figurar el número de registro en todas ellas. Si un solo número no está en la columna en el rango dado, el programa se detendrá:


::::::::::::::::::::
INSTRUCCIONES PARA EL USO DEL PROGRAMA DE ACTUALIZACIÓN ENLACES A FICHAS DEL MUSEO
::::::::::::::::::::

	Este programa permite actualizar automáticamente hasta 50 elementos en la columna de “Acceso Ficha” en el libro IDENTIFICACIÓN del inventario. Al ejecutarlo se rellenan las filas correspondientes a las piezas seleccionadas de esa columna, con los enlaces activos a sus respectivas fichas.
	Tras hacer click en “iniciar”, puede tardar unos segundos en comenzar, ya que debe recorrer todas las fichas antes de seleccionar las adecuadas.
	Para ello basta con hacer click en el botón “Actualizar Links”
Cuando no se encuentre ficha, se dejará en blanco la celda, y se advertirá al usuario de ello, pausando el programa.
A partir de ahí el proceso es análogo al programa que gestiona los iconos, pero el funcionamiento interno es distinto, por lo que asegurar que funciona correctamente tiene sus propias reglas.
LIMITACIONES DEL PROGRAMA
(Ver limitaciones del programa de Iconos)

ADVERTENCIA PARA EL CORRECTO FUNCIONAMIENTO DEL PROGRAMA
	Sobre el tratamiento de errores el proceder es análogo al de iconos.
	Para evitar problemas debemos asegurarnos de que las fichas se encuentran en la carpeta indicada. De lo contrario el programa nos advertirá de ello. 
	—Las fichas debe tener todas un nombre tal que comience así: “MUSEO XX.XXX-[…]”, siendo XX.XXX el número de pieza correspondiente. Si una ficha no tiene el nombre escrito correctamente siguiendo este patrón, la ficha no será detectada. Nótese el guion incluido, también imprescindible. Lo que se escriba a continuación es irrelevante. Esto admite también fichas de accesorios (XX.XXXa-), siempre con el guion.
	

ACTUALIZACIÓN
	Se ha añadido en el excel del Inventario una hoja llamada “Ajustes”.
	Si por algún motivo se modificara el emplazamiento de las fichas o las imágenes para los iconos, ahí se puede cambiar la carpeta para indicar a los programas la ruta en la que tienen que buscar fichas o imágenes. De esta forma las reglas mencionadas en las instrucciones se aplicarían para las carpetas indicadas por el usuario en ajustes. Para que los ajustes no desaparezcan debe guardarse el archivo de Excel. Si se realiza esto, probablemente se deban actualizar con el programa todos los links e iconos de la ficha para que siguieran siendo válidos haciendo referencia a las nuevas carpetas.

