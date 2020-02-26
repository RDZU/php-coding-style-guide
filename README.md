

# 🎩 Guía de estilo de código

![intro image](https://i.imgur.com/f3EB8XK.gif)

Como desarrolladores, uno de los pilares sobre los que debería cimentarse el trabajo en equipo es adoptar estándares para escribir código de mejor calidad con la finalidad de reducir la fricción de aprendizaje al enfrentarse a código ajeno gracias a un código más legible e interoperable.

  

## TL;DR

-   Conjunto de reglas para formatear código.
-   Reduce la fricción de aprendizaje al enfrentarse a código ajeno
-   PSR-12 vigente es el estándar que define las pautas de codificación
-   [Ejemplo de código](#ejemplo)
-   Configurar IDEs:
	-   [Phpstorm](#phpstorm)
    

  

----------

  
  

En el caso de PHP, a diferencia de otros lenguajes, no ha tenido nunca un estándar que establezca unas directrices de cómo escribir el código, siendo un ingrediente adicional para el famoso código espagueti.

  

El PHP-FIG (PHP-Framework Interop Group) es un grupo formado por personas, proyectos y organizaciones conocidos y reconocidos en el mundo PHP. Se han encargado de elaborar un conjunto de estándares que facilitan el desarrollo de aplicaciones.

  

Los estándares que definen las directrices de estilo de codificación vigentes son: PSR-1 y PSR-12 (sustituyendo a PSR-2).

  

## PSR-1: Basic Coding Standard

Son las pautas básicas. Este este documento no entraremos en detalle. Se puede consultar en: [https://www.php-fig.org/psr/psr-1/](https://www.php-fig.org/psr/psr-1/)

  

## PSR-12: Extended Coding Style

Extiende al estándar PSR-1 y sustituye al PSR-2 con las nuevas funcionalidades añadidas recientemente en PHP 7.x.

  

### Archivos

-   El código debe seguir la recomendación PSR-1
    
-   Todos los archivos deben usar el fin de línea UNIX LF
    
-   Todos los archivos deben terminar con una línea en blanco
    
-   La etiqueta de cierre ?> debe ser omitida de archivos que sólo contengan PHP
    

  

### Líneas

-   No hay un límite estricto para la longitud de las líneas pero de haberlo éste es de 120 caracteres. No obstante la recomendación es que las líneas no deberían tener más de 80 caracteres.
    
-   No debería haber espacios extras al final de las líneas que no estén en blanco
    
-   Se pueden añadir líneas en blanco para mejorar la legibilidad del código
    
-   No debe haber más de una instrucción por línea.
    

  
  

### Tabulado

-   Se deben emplear 4 espacios para tabular y no usar el carácter de tabulación para este propósito.
    

### Palabras clave de PHP

-   Las palabras clave de PHP deben estar escritas en minúscula al igual que las constantes true , false y null.
    
-   La forma corta de los tipos debe ser empleada en detrimento de la larga (por ejemplo, int en vez de integer ).
    

  

### Declare, use y namespace

-   El orden en la cabecera de un archivo PHP es el siguiente: etiqueta de apertura <?php , docblock , sentencias declare , sentencia namespace , sentencias use para importar clases, sentencias use para importar funciones, sentencias use para importar constantes, comentario recordando el propósito del código del archivo.
    
-   Cada uno de los bloques anteriores deben ir separados por una línea en blanco y no deben contener líneas en blanco.
    
-   Sólo debe haber un use por línea.
    
-   Después de todas las declaraciones use debe haber una línea en blanco.
    
-   Los enunciados imports no deben comenzar nunca con el caracter `\` y deben estar siempre “fully qualified”.
    

  

### Clases

-   Cualquier llave de cierre no puede ser seguida de un comentario o sentencia en la misma línea.
    
-   Cuando se instancia una nueva clase los paréntesis deben estar siempre presentes aunque no se estén pasando argumentos al constructor.
    
-   La llave de apertura debe ir en su propia línea y no puede ser precedida o seguida de una línea en blanco.
    
-   La llave de cierre debe ir en la siguiente línea después del cuerpo de la clase y no puede ir precedida por una línea en blanco.
    

### Extends e Implements

-   Las palabras clave extends e implements deben ser declaradas en la misma línea que el nombre de la clase.
    

  
Además, la lista de interfaces implementadas puede ser dividida en múltiplkes líneas, tabulando una vez cada línea así empleada. Si se emplea este estilo, el primer elemento de la lista debe aparecer en una nueva línea y sólo puede haber una interfaz por línea.

  

### Traits

-   El uso de la palabra clave use para implementar traits debe aparecer en la siguiente línea después de la llave de apertura.
    
-   Cada trait debe ir en su propia línea y tener su propio use para ser importado.
    
-   Después de las sentencias use para implementar traits debe haber una línea en blanco salvo que la clase no contenga nada más.
    

  

### Propiedades de clase

-   La visibilidad de cada propiedad y constante debe ser siempre declarada.
    
-   Cada propiedad debe ir en una línea.
    
-   La palabra clave var no puede ser usada para declarar una propiedad.
    
-   El nombre de las propiedades no puede llevar un guión bajo como prefijo de cara a indicar su visibilidad.
    

### Métodos y funciones

-   La visibilidad debe ser declarada en todos los métodos.
    
-   La llave de apertura debe ir en su propia línea y la llave de cierre en la siguiente línea después del cuerpo del método o función.
    
-   No debe haber un espacio después del paréntesis de apertura y no debe haber un espacio antes del paréntesis de cierre.
    
-   No puede haber un espacio antes de cada coma.
    
-   Debe haber un espacio después de cada coma.
    
-   Los argumentos que lleven un valor por defecto deben ir al final de la lista de argumentos.
    
-   En el caso de que sea necesario dividir los argumentos en diferentes líneas este es el estilo recomendado.
    
-   Cuando se especifique el tipo de retorno de la función, debe haber un espacio después de los dos puntos seguido del tipo. Tanto los dos puntos como el tipo deben estar en la misma línea que el paréntesis de cierre de la lista de argumentos sin espacio en blanco entre el paréntesis y los dos puntos.
    

  

### Calificadores abstract, final y static.

-   En el caso de estar presentes, las declaraciones abstract y final deben ir antes de la declaración de visibilidad de la clase.
    
-   En el caso de estar presente, la declaración static debe ir después de la declaración de visibilidad.
    

### Llamadas a funciones y métodos

-   No debe haber un espacio entre el nombre de la función y el paréntesis de apertura.
    
-   No debe haber un espacio después del paréntesis de apertura.
    
-   No debe haber un espacio antes del paréntesis de cierre.
    
-   En la lista de argumentos no debe haber un espacio antes de cada coma pero sí después de ella.
    
-   En el caso de que sea necesario separar en múltiples líneas la lista de argumentos éste es el estilo recomendado
    

  

### Estructuras de control de flujo

-   Debe haber un espacio después de las palabras if , else , for …
    
-   No debe haber un espacio después del paréntesis de apertura.
    
-   No debe haber un espacio antes del paréntesis de cierre.
    
-   Debe haber un espacio entre el paréntesis de cierre y la llave de apertura.
    
-   El cuerpo de la estructura de control debe ir tabulada una vez.
    
-   El paréntesis de cierre debe ir en la siguiente línea.
    
-   La palabra clave elseif debería ser empleada en vez de else if .
    
-   else y elseif deben ir en la misma línea que la llave de cierre de la anterior estructura de control.
    
-   La palabra clave case debe ser tabulada una vez con respecto a switch .
    
-   La palabra clave break debe ser tabulada al mismo nivel que el cuerpo del case .
    
-   Debe haber un comentario cuando no se emplee la palabra break dentro de un case de cara a que se “caiga” en el siguiente caso.
    

### Ejemplo

```
<?php

declare(strict_types=1);

namespace Vendor\Package;

use Vendor\Package\{ClassA as A, ClassB, ClassC as C};
use Vendor\Package\SomeNamespace\ClassD as D;

use function Vendor\Package\{functionA, functionB, functionC};

use const Vendor\Package\{ConstantA, ConstantB, ConstantC};

class Foo extends Bar implements FooInterface
{
    public function sampleFunction(int $a, int $b = null): array
    {
        if ($a === $b) {
            bar();
        } elseif ($a > $b) {
            $foo->bar($arg1);
        } else {
            BazClass::bar($arg2, $arg3);
        }
    }

    final public static function bar()
    {
        // method body
    }
}
```

  

## Configurar IDEs

#### PhpStorm

1.  Preferences
2.  Editor > Code Style > PHP 
3.  Set from > PSR-12
4.  OK
    
![](https://lh4.googleusercontent.com/0mpx_kIbGC738H8k12ARAo3HMDEaHQB2m5dX-1KFnVqkHf0QlXSquSCu2kHNo_9YXENZ4tgJngzwfudFx8ajYjnQxWkpDpNhdqABXpuROjy0AzeWTaVaC8gW7wfIJdKoINrtfUq1)
