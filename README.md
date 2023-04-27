# EncryptadorAluraLATAM

Encriptador realizado para el curso Oracle Next Education- Alura LATAM

Sintase libre de reproducir, modificar y/o utilizar el repositorio.

El Challenge consiste en crear desde cero un programa que encripte, desencripte y discrimine entre minusculas, mayusculas y acentos. Ademas debe contar con un diseño ya establecido, de todas maneras se agrego un modo nocturno y algunos cambios de colores e imagenes, pero se intento mantener el estilo dentro de lo requerido. 


Puedes probar el Encryptador aquí: https://fedelpx.github.io/EncryptadorAluraLATAM/

**This code defines a web page with an interactive feature that allows users to encrypt and decrypt messages.

The code uses JavaScript to manipulate the HTML elements of the page, and it includes four main functions: mostrar(), actualizarPantalla(), encriptarMensaje(), desencriptarMensaje(), and copiarTexto().**

# javasScriptLog.

Este codigo define una serie de funciones que son usadas para encriptar y desencriptar mensajes ingresados por el usuario.

*La función "mostrar(mensaje)" toma el string "mensaje" y actualiza el contenido del HTML del elemento con el id "resultado" para mostrar el mensaje. 

*La función "actualizarPantalla()" es usada para para mostrar ciertos elementos del HTML y ocultar otros. Es llamada por las funciones "encriptarMensaje" y "desencriptarMensaje" para mostrar el mensaje depues de ser encriptado o desencriptado.

*La función "encriptarMensaje()" recoge el texto ingresado por el usuario en un <input>"texto" y despues aplica una sustitución cifrada para encriptar el mensaje.El mensaje encriptado es mostrado en la pagina usando la función "mostrar(mensaje)".

*La función "desencriptarMensaje()" toma el mensaje encriptado ingresado por el usuario en el <input>"texto" y luego usa un conjunto de remplazos para desencriptar el mensaje. El mensaje desencriptado es mostrado en la pagina usando la función "mostrar(mensaje)".

*La función "copiarTexto()" es usada para copiar el mensaje encriptado o desencriptado cuando el usuario clickea en el boton con el id"copiar".

Por ultimo el codigo tambien programa eventos cuando el usuario clickea en los botones con el id: "encriptar", "desencriptar", "copiar" y cuando el usuario clickea en el diamante, lo que cambia al modo nocturno. 

-----------------------------------------------------------------------------------

 Las funciones "encriptarMensaje()" y desencriptarMensaje()

"encriptarMensaje" 

Esta función es llamdada cuando el usuario clickea en el boton //Encriptar// de la pagina. Primero, recoge el texto ingresado por el usuario en el HTML:
<input>"texto", entonces inicia una variable con string vacio llamada "secreto" para retener el mensaje encriptado.

La función entonces chequea que la variable "mensaje" no es un string vacio o contiene letras mayusculas o acentuadas y tambien controla que el mensaje tenga cierta longitud usando la función "trim()". Si alguna de de estas condiciones no son cumplidas, muestra una alerta al usuario para que ingrese minusculas sin acento.

Si las condiciones son cumplidas, la función comienza un loop por cada carácter del string "mensaje" usando 'for' {Por cada carácter usa la declaración 'switch' que chequea si es igual a alguna de las vocales a,e,i,o,u. Si el carácter es una vocal, el codigo correspondiente es adjuntado al string de la vareable "secreto". Si no es una vocal el carácter original es adjuntado al string "secreto".

Una vez que el loop es completado, la funcion "actualizarPantalla()" es llamada para actualizar lo que se muestra en la pagina. Por ultimo el <input>"texto" es limpiado.


"desencriptarMensaje()"

Esta función es llamada cuando el usuario clickea en le boton //Desencriptar// de la pagina. Sigue un patron similar a "encriptarMensaje()" con algunas diferencias fundamemntales.

Primero toma el texto ingresado por el usuario en HTML: id="texto" entonces incia dos arrays: "codigos" y "letras". El array "codigos" contiene expresiones que son iguales a las palabras en codigo usadas en el proceso de encriptado, mientras el array "letras" contiene las correspondientes vocales que deberían usarse para remplazar las palabras en codigo.

La función entonces chequea si la variaboe "mensaje" es un string vacio y hace las comprobaciones de mayus, acentos y longitud del mensaje. Si alguna de esas condiciones no son cumplidas, muestra un mensaje de alerta a el usuario para que ingrese minusculas y palabras sin acentuar. 

Si las condiciones son cumplidas, la funcion inicia un loop a traves de cada item en el array "codigos" usando 'for'. Por cada item, usa la función "replaceAll()" para reemplazar todas las concatenaciones de la palabra clave en el string "mensaje" con la correspondiente vocal del array "letras".

Una vez el loop esta completo, la función "actualizarPantalla()" es llamada para actualizar lo que se muestra en la pagina. La función "mostrar()" es llamada con el valor de la variable "mensaje" (que ahora contiene el mensaje desencriptado) como un argumento para mostrar el mensaje desencriptado en la pagina. Finalmente el valor del <input>"texto" es borrada. 






