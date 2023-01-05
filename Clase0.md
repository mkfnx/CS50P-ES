
# [Clase 0](https://cs50.harvard.edu/python/2022/notes/0/#lecture-0)

-   [Creando código con Python](https://cs50.harvard.edu/python/2022/notes/0/#creating-code-with-python)
-   [Funciones](https://cs50.harvard.edu/python/2022/notes/0/#functions)
-   [Errores (Bugs)](https://cs50.harvard.edu/python/2022/notes/0/#bugs)
-   [Mejorando tu primer programa de Python](https://cs50.harvard.edu/python/2022/notes/0/#improving-your-first-python-program)
    -   [Variables](https://cs50.harvard.edu/python/2022/notes/0/#variables)
    -   [Comentarios](https://cs50.harvard.edu/python/2022/notes/0/#comments)
    -   [Pseudocódigo](https://cs50.harvard.edu/python/2022/notes/0/#pseudocode)
-   [Más mejoras a tu primer programa de Python](https://cs50.harvard.edu/python/2022/notes/0/#further-improving-your-first-python-program)
-   [Cadenas (Strings) y Parámetros](https://cs50.harvard.edu/python/2022/notes/0/#strings-and-paremeters)
    -   [Un pequeño problema con las comillas](https://cs50.harvard.edu/python/2022/notes/0/#a-small-problem-with-quotation-marks)
-   [Dando formato a las Strings](https://cs50.harvard.edu/python/2022/notes/0/#formatting-strings)
-   [Más sobre las Strings](https://cs50.harvard.edu/python/2022/notes/0/#more-on-strings)
-   [Enteros (Integer) or int](https://cs50.harvard.edu/python/2022/notes/0/#integers-or-int)
-   [La legibilidad primero](https://cs50.harvard.edu/python/2022/notes/0/#readability-wins)
-   [Lo básico de los Float](https://cs50.harvard.edu/python/2022/notes/0/#float-basics)
-   [Más sobre Floats](https://cs50.harvard.edu/python/2022/notes/0/#more-on-floats)
-   [Def](https://cs50.harvard.edu/python/2022/notes/0/#def)
-   [Devolviendo valores (return)](https://cs50.harvard.edu/python/2022/notes/0/#returning-values)
-   [Resumen](https://cs50.harvard.edu/python/2022/notes/0/#summing-up)

## [Creando código con Python](https://cs50.harvard.edu/python/2022/notes/0/#creating-code-with-python)

-   VS Code es un tipo particular de editor de texto [incluye herramientas de programación como compiladores]. En la parte de arriba verás el editor de texto y en la parte de abajo verás una terminal, en ella puedes ejecutar comandos.
-   En la terminal, ejecuta el comando  `code hello.py`  para comenzar a programar.
-   En el editor de texto, escribe  `print("hello, world")`. Es un programa típico que casi todos los programadores escriben cuando están aprendiendo.
-   Para ejecutar este programa da click en la sección de la terminal. Ahí puedes escribir comandos. Junto al símbolo de moneda escribe  `python hello.py`  y presiona enter en tu teclado.
-   Las computadoras solo entienden ceros y unos, Por lo tanto, cuando ejecutas el comando  `python hello.py`, python interpreta el texto del archivo  `hello.py`  y lo traduce a los ceros y unos que la computadora puede entender.
-   El resultado de ejecutar el programa  `python hello.py`  es  `hello, world`.
-   ¡Felicidades! Creaste tu primer programa.

## [Funciones](https://cs50.harvard.edu/python/2022/notes/0/#functions)

-   Las funciones son acciones que la computadora o el lenguaje de programación ya sabe ejecutar, normalmente usan verbos en el nombre.
-   En tu programa  `hello.py`, la función  `print` sabe cómo imprimir valores en la terminal.
-   La función  `print`  toma argumentos. En este caso,  `"hello, world"`  son los argumentos de la función `print`.

## [Errores (Bugs)](https://cs50.harvard.edu/python/2022/notes/0/#bugs)

-   Cometer errores es algo natural de la programación. Son solo otro problema a resolver, así que no te desanimes. Es parte del proceso de convertirse en un gran programador.
-   Imagina que en nuestro programa  `hello.py` accidentalmente escribimos  `print("hello, world"`  nota que al final falta un  `)`. Si cometemos ese error (aún de forma intencional), el compilador mostrará un error en la terminal.
-   Normalmente estos mensajes dan información sobre tu error y pistas sobre cómo solucionarlos, aunque en algunas ocasiones los mensajes pueden ser algo confusos.

## [Mejorando tu primer programa](https://cs50.harvard.edu/python/2022/notes/0/#improving-your-first-python-program)

-   Vamos a personalizar nuestro programa `hello.py` usando la función.  `input`. Esta función toma el parámetro `prompt` como argumento. Editamos nuestro co4digo para que quede de esta forma
	```python
	input("What's your name? ")
	print("hello, world")
	```
    
-   Pero si solo hacemos este cambio, no estamos usando el valor que el usuario ingresó. Para ello, necesitamos presentar el concepto de "variables"

### [Variables](https://cs50.harvard.edu/python/2022/notes/0/#variables)

-   Una variable es un contenedor para un valor en nuestro programa.
-   Vamos a agregar una variable en nuestro programa con el siguiente código
    
	```python
	name = input("What's your name? ")
	print("hello, world")
	```
    
    Nota el signo  `=`  a la mitad de la instrucción  `name = input("Cuál es tu nombre? ")`, esto tiene un significado particular en programación. Este símbolo asigna el valor de la derecha a la variable de la izquierda. Por lo tanto el valor devuelto por la instrucción  `input("What's your name? ")`  se asigna a  `name`.
    
-   Nuestro siguiente código se ve de esta manera, sin embargo tiene un error.
    
	```python
	name = input("What's your name? ")
	print("hello, name")
	```
    
-   El programa imprime  `hola, name`  en la terminal sin importar lo que el usuario escriba.
-   Nuestra siguiente versión del código se ve así:
    
	```python
	name = input("What's your name? ")
	print("hello,")
	print(name)
	```
    
-  El resultado en la terminal será
    
	```
	What's your name? David
	hello
	David
	```
    
-   Ya nos acercamos al resultado que buscamos!
    
-   En la documentación de Python puedes aprender más sobre [tipos de datos](https://docs.python.org/3/library/datatypes.html).

### [Comentarios](https://cs50.harvard.edu/python/2022/notes/0/#comments)

-   Los comentarios son una forma en la que los programadores pueden colocar notas sobre lo que hace su programa e informar sobre ello a otros personas que trabajen con el código.
-   Un ejemplo de código con comentarios es el siguiente:
    
	```python
	# Ask the user for their name
	name = input("What's your name? ")
	print("hello,")
	print(name)
	```
    
-   Otro uso común de los comentarios es crear listas y recordatorios para cuando vuelvas a trabajar con ese código.

### [Pseudocódigo](https://cs50.harvard.edu/python/2022/notes/0/#pseudocode)

-   Usaremos comentarios de pseudocódigo para anotar tareas a realizar, especialmente cuando aún no tienes claro como hacer algo. Por ejemplo en el siguiente código:
    
	```python
	# Ask the user for their name
	name = input("What's your name? ")

	# Print hello
	print("hello,")

	# Print the name inputted
	print(name)
	```
    

## [Más mejoras a tu primer programa de Python](https://cs50.harvard.edu/python/2022/notes/0/#further-improving-your-first-python-program)

-   Así se ve la siguiente versión de nuestro:
    
	```python
	# Ask the user for their name
	name = input("What's your name? ")

	# Print hello and the inputted name
	print("hello, " + name)
	```
    
-   Algunas funciones toman argumentos.
-   Usamos una coma  `,`  para enviar varios argumentos:
    
	```python
	# Ask the user for their name
	name = input("What's your name? ")

	# Print hello and the inputted name
	print("hello,", name)
	```
    
    La salida en la terminal, si escribimos “David” será  `hola, David`. Éxito.
    

## [Strings (Cadenas de texto) y Parámetros](https://cs50.harvard.edu/python/2022/notes/0/#strings-and-paremeters)

-   Una string, conocida como  `str`  en Python, es una secuencia de texto.
-   En una versión anterior de nuestro código, nuestro resultado se mostraba en varias líneas de la terminal:
    
	```python
	# Ask the user for their name
	name = input("What's your name? ")
	print("hello,")
	print(name)
	```
    
-   Los argumentos que reciben las funciones influyen en su comportamiento y resultado. En la documentación de [`print`](https://docs.python.org/3/library/functions.html#print) podemos aprender sobre los argumentos de la función `print`.
-   Según vemos en la documentación, la función `print` automáticamente incluye un parámetro  `end='\n'` Esto hace que la función `print` automáticamente inserte un salto de línea. La función `print` toma un argumento llamado `end` cuyo valor por default es el salto de línea.
-   Podemos proporcionar nuestro propio argumento para el parámetro  `end`  para que no sea cree una nueva línea si no lo necesitamos
-   Modificamos nuestro código para que quede la siguiente forma:
    
	```python
	# Ask the user for their name
	name = input("What's your name? ")
	print("hello,", end="")
	print(name)
	```
    
    Mediante el fragmento de código  `end=""` estamos sobre-escribiendo el valor por defecto de  `end`  para que la instrucción que incluye ese parámetro con ese valor no cree una nueva línea .
    
-   Cualquier función puede solicitar parámetros/argumentos.
    
-   En la documentación de Python puedes aprender más sobre la función  [`print`](https://docs.python.org/3/library/functions.html#print).

### [Pequeño problema con las comillas](https://cs50.harvard.edu/python/2022/notes/0/#a-small-problem-with-quotation-marks)

-   Agregar comillas a las strings puede ser confuso.
-   La instrucción `print("hello,"friend"")`  no funcionará y el compilador mostrará un error.
-   Generalmente hay dos formas de solucionar algo así. La primera es cambiar el tipo de las comillas, de simples a dobles o viceversa.
-   La instrucción  `print("hello, \"friend\"")` muestra otra solución común. Las diagonales invertidas le indican al compilador que el símbolo a su derecha no debe ser interpretado como el final de la cadena para así evitar el error de compilación.

## [Dando formato a las strings](https://cs50.harvard.edu/python/2022/notes/0/#formatting-strings)

-   Probablemente la forma más elegante de usar strings es la siguiente:
    
    ```python
    # Ask the user for their name
    name = input("What's your name? ")
    print(f"hello, {name}")
    ```
    
    Observa que en la instrucción `print(f"hello, {name}")` hay una  `f` al principio de la String. Esta  `f`  es un indicador especial para que Python trate a la string de forma diferente. Este estilo de formato se usará frecuentemente en el curso.
    

## [Más sobre las Strings](https://cs50.harvard.edu/python/2022/notes/0/#more-on-strings)

-   Nunca debes esperar que el usuario coopere y se comporte como esperamos. Por lo tanto, necesitas asegurarte de verificar los datos que los usuarios ingresan a tus programas.
-   Las String de Python tienen un método para eliminar espacios en blanco.
-   Puedes eliminar los espacios en blanco a la izquierda y a la derecha de la cadena que ingresa el usuario con la instrucción  `name = name.strip()`. Con este cambio tu código se verá de la siguiente forma:
    
    ```python
    # Ask the user for their name
    name = input("What's your name? ")
    
    # Remove whitespace from the str
    name = name.strip()
    
    # Print the output
    print(f"hello, {name}")
    ```
    
    Al ejecutar esta versión del programa los espacios en blanco a los extremos de la cadena serán eliminados.
    
-   El método  `title` convertirá a mayúscula la primer letra de cada palabra de una String:
    
    ```python
    # Ask the user for their name
    name = input("What's your name? ")
    
    # Remove whitespace from the str
    name = name.strip()
    
    # Capitalize the first letter of each word
    name = name.title()
    
    # Print the output
    print(f"hello, {name}")
    ```
    
-   Para este momento, ya debes estar muy cansado de escribir el comando `python` en la terminal cada vez que ejecutas tu programa, así que puedes usar la tecla de flecha arriba para mostrar los comandos ejecutados recientemente .
-   Podemos modificar el código para hacerlo más corto sin que se modifique su resultado:
    
    ```python
    # Ask the user for their name
    name = input("What's your name? ")
    
    # Remove whitespace from the str and capitalize the first letter of each word
    name = name.strip().title()
    
    # Print the output
    print(f"hello, {name}")
    ```
    
-   Podemos modificarlo más!
    
    ```python
    # Ask the user for their name, remove whitespace from the str and capitalize the first letter of each word
    name = input("What's your name? ").strip().title()
    
    # Print the output
    print(f"hello, {name}")
    ```
    
-   En la documentación de Python puedes aprender más sobre las Strings  [`str`](https://docs.python.org/3/library/stdtypes.html#str)

## [Integers (Enteros) o int](https://cs50.harvard.edu/python/2022/notes/0/#integers-or-int)

-   En Python un número entero se conoce como  `int`.
-   Los símbolos como +, -, *, /, % nos resultan familiares para realizar operaciones matemáticas. Aunque la operación de Python correspondiente al último símbolo`%` tal vez no te resulte tan familiar, se conoce como módulo o residuo.
-   También puedes ejecutar el comando `python` sin indicar ningún programa a ejecutar. Al hacerlo verás el texto  `>>>` en la terminal. Este es el modo "interactivo" del interprete de Python. Si escribes  `1+1`  el interprete realizará esa operación. No usaremos mucho este modo de ejecución en el curso, pero es útil para realizar pequeñas pruebas de funcionamiento.
-   De vuelta a VS Code, escribimos  `code calculator.py` en la terminal para crear un nuevo archivo en el que vamos a programar una calculadora.
-   Primero declaramos algunas variables.
    
    ```python
    x = 1
    y = 2
    
    z = x + y
    
    print(z)
    ```
    
    Cuando ejecutemos  `python calculator.py`  obtendremos el valor `3` en la terminal. Podemos hacer esto más interactivo usando la función  `input`.
    
    ```python
    x = input("What's x? ")
    y = input("What's y? ")
    
    z = x + y
    
    print(z)
    ```
    
-   Al ejecutar este programa vemos que da el resultado incorrecto de  `12`. Por qué pasa esto?
-   Ya vimos antes como el símbolo  `+`  se usa para unir o "concatenar" dos cadenas. Lo que ingresas al programa mediante tu teclado se interpreta com texto, es decir como una String. Por lo tanto debes indicar a Python que queremos que este valor se interprete como un `int`, esto se conoce como **conversión de tipo** o **cast**. Realizamos dicha conversión de la siguiente forma:
    
    ```python
    x = input("What's x? ")
    y = input("What's y? ")
    
    z = int(x) + int(y)
    
    print(z)
    ```
    
    Ahora el resultado es correcto.
    
-   Una mejor versión de nuestro programa es la siguiente:
    
    ```python
    x = int(input("What's x? "))
    y = int(input("What's y? "))
    
    print(x + y)
    ```
    
    En este ejemplo vemos que podemos ejecutar funciones dentro de funciones. La función que esté "más adentro" se ejecutará primero, y luego las más externas. Aquí se ejecuta primero la función `input`  Y luego la función  `int`.
    
-  En la documentación de Python puedes aprender más sobre [`int`](https://docs.python.org/3/library/functions.html?highlight=float#int).

## [La facilidad de lectura es primero](https://cs50.harvard.edu/python/2022/notes/0/#readability-wins)

-   Siempre habrá distintas formas de estructurar nuestro código para dar solución a un problema.
-   Recuerda que siempre debes procurar que tu código no sea difícil de leer y que puedes usar comentarios para dar información necesaria sobre a función del código.

## [Lo básico de los Float](https://cs50.harvard.edu/python/2022/notes/0/#float-basics)

-   Un valor float (["punto flotante"](https://es.wikipedia.org/wiki/Coma_flotante)) es un número real con un punto decimal, por ejemplo  `0.52`.
-   El siguiente código trabaja con valores float:
    
    ```python
    x = float(input("What's x? "))
    y = float(input("What's y? "))
    
    print(x + y)
    ```
    
    Este cambio permite que ingresemos valores como  `1.2`  y  `3.4`  y así obtener un resultado de  `4.6`.
    
-   Imaginemos que queremos redondear el resultado al valor entero más cercano. Python cuenta con la función `round` cuya documentación nos dice que recibe los parámetros `round(number[n, ndigits])`. Los corchetes indican parámetros opcionales. Así que para redondear al entero más cercano podemos ejecutar la instrucción `round(n)`.  Así se vería en nuestro código:
    
    ```python
    # Get the user's input
    x = float(input("What's x? "))
    y = float(input("What's y? "))
    
    # Create a rounded result
    z = round(x + y)
    
    # Print the result
    print(z)
    ```
    
-   Y si quisieramos dar formato a números largos? Por ejemplo, en lugar de `1000`,  podríamos querer ver `1,000`. Para esto modifica tu código para que quede de la siguiente forma.
    
    ```python
    # Get the user's input
    x = float(input("What's x? "))
    y = float(input("What's y? "))
    
    # Create a rounded result
    z = round(x + y)
    
    # Print the formatted result
    print(f"{z:,}")
    ```
    
    La instrucción `print(f"{z:,}")`  indica que se debe insertar una coma como separador en números largos como `1,000` o `2,500`.
    

## [Más sobre los Floats](https://cs50.harvard.edu/python/2022/notes/0/#more-on-floats)

-   Para redondear números flotantes modifica tu código de la siguiente forma:
    
    ```python
    # Get the user's input
    x = float(input("What's x? "))
    y = float(input("What's y? "))
    
    # Calculate the result
    z = x / y
    
    # Print the result
    print(z)
    ```
    
    Cuándo ingresas `2`  para la variable `x` y  `3`  para la variable `y`, el resultado `z` será  `0.6666666666`.
    
-   Para redondear este resultado "hacia abajo" usamos el siguiente código:
    
    ```python
    # Get the user's input
    x = float(input("What's x? "))
    y = float(input("What's y? "))
    
    # Calculate the result and round
    z = round(x / y, 2)
    
    # Print the result
    print(z)
    ```
    
-   También podemos usar  `fstring` para dar formato al resultado:
    
    ```python
    # Get the user's input
    x = float(input("What's x? "))
    y = float(input("What's y? "))
    
    # Calculate the result
    z = x / y
    
    # Print the result
    print(f"{z:.2f}")
    ```
    
    Aunque en general, dar formato con  `fstring`  es algo más difícil de leer.
    
-   En la documentación de Python puedes aprender más sobre  [`float`](https://docs.python.org/3/library/functions.html?highlight=float#float).
    

## [Def](https://cs50.harvard.edu/python/2022/notes/0/#def)

-   No sería genial poder crear nuestras propias funciones?
-   Regresemos a nuestra versión final de  `hello.py`  ejecutando  `code hello.py`  en la terminal. Tu código se debe ver de la siguiente forma:
    
    ```python
    # Ask the user for their name, remove whitespace from the str and capitalize the first letter of each word
    name = input("What's your name? ").strip().title()
    
    # Print the output
    print(f"hello, {name}")
    ```
    
    Podemos crear nuestra propia funciona encargada de decir “hello” por nosotros!
    
-   Escribimos el siguiente código:
    
    ```python
    name = input("What's your name? ")
    hello()
    print(name)
    
    ```
    
    Al intentar ejecutar este código, el compilador mostrará un error debido a que no existe una función llamada `hello`.
    
-   Podemos crear nuestra propia función  `hello`  de la siguiente forma:
    
    ```python
    def hello():
        print("hello")
    
    
    name = input("What's your name? ")
    hello()
    print(name)
    ```
    
    Observa que todo lo que está debajo de la instrucción  `def hello()`  está ["indentado"](https://es.wikipedia.org/wiki/Estilo_de_sangrado). Python usa indentation para indicar que forma parte de cada función. Por lo tanto, todo el contenido de nuestra función  `hello`  debe estar espaciado, de lo contrario Python interpretará que no es parte de la función. Al ejecutar  `python hello.py`  en la terminal, verás que no estamos obteniendo el resultado esperado.
    
-   Nuestra siguiente versión del código es la siguiente:
    
    ```python
    # Create our own function
    def hello(to):
        print("hello,", to)
    
    
    # Output using our own function
    name = input("What's your name? ")
    hello(name)
    ```
    
    En las primeras lineas creamos la función  `hello` . Esta vez estamos indicando que la función toma un parámetro: una variable llamada  `to`. Por lo tanto cuando llamemos a la función  `hello(name)`  la computadora enviará la variable  `name`  a la función  `hello` con el nombre de  `to`. Al ejecutar  `python hello.py`  en la terminal, verás que la salida del programa es más cercana a lo que queremos.
    
-  Podemos ajustar el código para incluir un valor por defecto para el parámetro `to` de la función  `hello`:
    
    ```python
    # Create our own function
    def hello(to="world"):
        print("hello,", to)
    
    
    # Output using our own function
    name = input("What's your name? ")
    hello(name)
    
    # Output without passing the expected arguments
    hello()
    ```
    
    Vuelve a ejecutar el código y observa cómo la primera llamada a la función  `hello` imprime el nombre que indicamos, mientras que el segundo, al que no le enviamos un valor, imprime el valor por defecto de  `hello, world`.
    
-   También podemos definir nuestra función `hello` en la parte de abajo del archivo.
    
    ```python
    def main():
    
        # Output using our own function
        name = input("What's your name? ")
        hello(name)
    
        # Output without passing the expected arguments
        hello()
    
    
    # Create our own function
    def hello(to="world"):
        print("hello,", to)
    ```
    
    Esta versión dará algunos errores ya que al ejecutar  `python hello.py`  no pasa nada! Esto es porque no tenemos nada en nuestro código que invoque a la función  `main`, la principal de nuestro programa.
    
-   En la siguiente modificación ya incluimos una llamada a la función  `main`  lo cual hará que nuestro programa funcione adecuadamente:
    
    ```python
    def main():
    
        # Output using our own function
        name = input("What's your name? ")
        hello(name)
    
        # Output without passing the expected arguments
        hello()
    
    
    # Create our own function
    def hello(to="world"):
        print("hello,", to)
    
    
    main()
    ```
    

## [Devolviendo valores (return)](https://cs50.harvard.edu/python/2022/notes/0/#returning-values)

-   Hay situaciones en las que no solo queremos que una función realice una acción sino que también queremos que devuelva un valor al contexto en el que fue llamada. Por ejemplo, en lugar de solo realizar una operación como  `x + y`, podrías necesitar que la función comunique el resultado de esa operación para que la puedas usar en otra parte de tu programa. A esta acción de “devolver” un valor lo conocemos como  `return`.
-   Volviendo a nuestro programa  `calculator.py` ejecutando  `code calculator.py`. Ajusta el código como se ve a continuación:
    
    ```python
    def main():
        x = int(input("What's x? "))
        print("x squared is", square(x))
    
    
    def square(n):
        return n * n
    
    
    main()
    ```
    
    Aquí observamos que el valor  `x`  es enviado a la función `square` y qie luego la función devuelve el resultado de la operación  que ejecuta (`x * x`).
