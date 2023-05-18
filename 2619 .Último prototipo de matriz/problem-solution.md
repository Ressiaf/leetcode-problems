El enunciado de la tarea establece que necesitamos escribir un código que mejore todas las matrices para que podamos llamar al método array.last() y obtener el último elemento de la matriz. Si la matriz está vacía, el método debe devolver -1.

Dado que queremos agregar esta funcionalidad a todas las matrices, la mejor manera de hacerlo es extendiendo el prototipo del objeto Array. En JavaScript, el prototipo es un objeto del que heredan todos los demás objetos de una determinada clase.

Entonces, creamos una función llamada Array.prototype.last para extender el prototipo del objeto Array. Esto significa que todos los objetos de tipo Array tendrán acceso a este método.

Dentro de la función Array.prototype.last, verificamos si la longitud de la matriz (this.length) es igual a cero. Si es así, significa que la matriz está vacía y no tiene elementos, por lo que devolvemos -1.

Si la longitud de la matriz no es cero, eso significa que hay elementos en ella. Para acceder al último elemento, podemos usar this[this.length - 1]. El índice del último elemento es la longitud de la matriz menos uno, porque los índices en JavaScript comienzan en cero.

Finalmente, cuando llamamos al método array.last() en una matriz, devuelve el último elemento si hay elementos en la matriz, de lo contrario, devuelve -1.