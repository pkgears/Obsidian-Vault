
#python #programming #decorators

Los decoradores en Python son una herramienta poderosa y flexible que permite modificar o extender el comportamiento de funciones o métodos sin cambiar su código fuente. Son ampliamente utilizados para la metaprogramación y pueden ser muy útiles en diversas situaciones, como la validación, la autorización, el registro de eventos, y más.
### Concepto Básico
Un decorador en Python es una función que recibe otra función como argumento y devuelve una nueva función que generalmente extiende o modifica el comportamiento de la función original.
### [[Ejemplo Decorators en python]]
Supongamos que queremos crear un decorador que imprima un mensaje antes y después de la ejecución de una función. Aquí está cómo se puede hacer:

```python
# Definir el decorador
def mi_decorador(func):
    def envoltura():
        print("Algo antes de la función")
        func()
        print("Algo después de la función")
    return envoltura

# Aplicar el decorador
@mi_decorador
def di_hola():
    print("¡Hola!")

# Llamar a la función decorada
di_hola()
```

```code
Algo antes de la función
¡Hola!
Algo después de la función
```
