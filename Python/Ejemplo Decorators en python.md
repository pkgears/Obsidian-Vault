
#decorators #python  #programming #examples

1. **Definición del [Decorator](Python/Decorators)**:
	```python
    def mi_decorador(func):
        def envoltura():
            print("Algo antes de la función")
            func()
            print("Algo después de la función")
        return envoltura
	```
    - `mi_decorador` es una función que toma otra función `func` como argumento.
    - Dentro de `mi_decorador`, definimos una función `envoltura` que agrega comportamiento adicional antes y después de llamar a `func`.
    - `mi_decorador` devuelve la función `envoltura`.
2. **Aplicar el [Decorador](Python/Decorators.md)**:
    
    ```python
    @mi_decorador
    def di_hola():
        print("¡Hola!")
    ```
    - La línea `@mi_decorador` antes de `def di_hola():` aplica el decorador `mi_decorador` a la función `di_hola`.
    - Esto es equivalente a `di_hola = mi_decorador(di_hola)`.
3. **Llamar a la Función Decorada**:
    
    ```python
	di_hola()
    ```
    - Al llamar a `di_hola()`, en realidad estamos llamando a `envoltura()`, que es la función devuelta por `mi_decorador`.
    - La salida será:

	```code
	Algo antes de la función
	¡Hola!
	Algo después de la función
	```