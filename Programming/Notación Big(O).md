### **¿Qué es la notación Big-O?**

#programming 

La notación Big-O describe el **límite superior** del crecimiento de una función. En el contexto de algoritmos, se usa para indicar cuánto tiempo o espacio requiere un algoritmo en función del tamaño de la entrada.

- **Fórmula general**: O(f(n))
    
    - f(n) es una función que representa el crecimiento del tiempo o espacio en función de n (tamaño de la entrada).
        
    - O indica que el crecimiento no superará a f(n) en el peor caso.

---

### **¿Por qué es importante?**

1. **Comparación de algoritmos**: Permite comparar la eficiencia de diferentes algoritmos.
    
2. **Diseño de software**: Ayuda a elegir el algoritmo más adecuado para un problema.
    
3. **Optimización**: Identifica cuellos de botella en el rendimiento.
    

---

### **Complejidades comunes de Big-O**:

Aquí tienes una lista de las complejidades más comunes, ordenadas de menor a mayor:

1. **O(1) - Constante**:
    
    - El tiempo o espacio es constante, no depende de n.
    - Ejemplo: Acceder a un elemento de un arreglo por índice.
		```ruby
		def access_element(arr, index)
		  arr[index]
		end
		``` 
	- Complejidad: O(1)O(1), porque el acceso a un elemento en un arreglo es constante.
2. **O(logn) - Logarítmica**:
    
    - El tiempo o espacio crece logarítmicamente con n.
    - Ejemplo: Búsqueda binaria en un arreglo ordenado.
		```ruby
		def binary_search(arr, target)
		  low = 0
		  high = arr.length - 1
		  while low <= high
			mid = (low + high) / 2
			if arr[mid] == target
			  return mid
			elsif arr[mid] < target
			  low = mid + 1
			else
			  high = mid - 1
			end
		  end
		  -1
		end
		```
	- Complejidad: O(logn), porque el espacio de búsqueda se reduce a la mitad en cada iteración.
3. **O(n) - Lineal**:
    
    - El tiempo o espacio crece proporcionalmente a n.
    - Ejemplo: Recorrer un arreglo de tamaño n.
		```ruby
		def traverse_array(arr)
		  arr.each do |element|
		    puts element
		  end
		end
		```
	- Complejidad: O(n), porque el bucle se ejecuta n veces.
4. **O(nlogn) - Linealítmica**:
    
    - El tiempo o espacio crece en proporción a nlogn.
    - Ejemplo: Algoritmos de ordenación eficientes como Merge Sort o Quick Sort.
	```ruby
		def merge_sort(arr)
		  return arr if arr.length <= 1
		
		  mid = arr.length / 2
		  left = merge_sort(arr[0...mid])
		  right = merge_sort(arr[mid...arr.length])
		  merge(left, right)
		end
		
		def merge(left, right)
		  sorted = []
		  until left.empty? || right.empty?
			if left.first <= right.first
			  sorted << left.shift
			else
			  sorted << right.shift
			end
		  end
		  sorted + left + right
		end
	```
	- Complejidad: O(nlogn), porque divide el arreglo en mitades (logn) y luego las fusiona (n).
5. **O(n2) - Cuadrática**:
    
    - El tiempo o espacio crece proporcionalmente a n2.
    - Ejemplo: Algoritmos de ordenación ineficientes como Bubble Sort o Insertion Sort.
	```ruby
		def bubble_sort(arr)
		  n = arr.length
		  for i in 0...n
		    for j in 0...n-i-1
		      if arr[j] > arr[j+1]
		        arr[j], arr[j+1] = arr[j+1], arr[j]
		      end
		    end
		  end
		  arr
		end
	```
	- Complejidad: O(n2), porque hay dos bucles anidados que recorren el arreglo.
6. **O(2n) - Exponencial**:
    
    - El tiempo o espacio crece exponencialmente con n.
    - Ejemplo: Resolver el problema de la mochila con fuerza bruta.
	```ruby
		def fibonacci(n)
		  return n if n <= 1
		  fibonacci(n-1) + fibonacci(n-2)
		end
	```
	- Complejidad: O(2n), porque cada llamada genera dos llamadas adicionales.
7. **O(n!) - Factorial**:
    
    - El tiempo o espacio crece factorialmente con n.
    - Ejemplo: Generar todas las permutaciones de un conjunto.
	```ruby
	def permutations(arr)
	  return [arr] if arr.length <= 1
	
	  result = []
	  arr.each_with_index do |element, index|
	    rest = arr[0...index] + arr[index+1...arr.length]
	    permutations(rest).each do |perm|
	      result << [element] + perm
	    end
	  end
	  result
	end
	```
	- Complejidad: O(n!), porque el número de permutaciones de n elementos es n!.




![[Pasted image 20250130210653.png]]

*** Notas***
Cuando algo crece logarítmicamente con respecto a una variable, significa que su crecimiento es **muy lento** y **altamente eficiente**. Esto es especialmente útil en algoritmos donde el tamaño de la entrada puede ser grande, como en búsquedas, árboles binarios o algoritmos de divide y vencerás.