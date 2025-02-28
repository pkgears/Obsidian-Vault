#programming #data-structures

### **Conceptos básicos**:

1. **Nodo**: Unidad básica del árbol. Contiene un valor (dato) y referencias a sus hijos.
    
2. **Raíz**: El nodo superior del árbol, desde donde comienza la estructura.
    
3. **Hijos**: Los nodos que están directamente debajo de un nodo. En un árbol binario, cada nodo tiene como máximo dos hijos: **hijo izquierdo** e **hijo derecho**.
    
4. **Hoja**: Un nodo que no tiene hijos.
    
5. **Subárbol**: Un árbol que forma parte de otro árbol más grande.
    
6. **Altura**: La longitud del camino más largo desde la raíz hasta una hoja.
    

---

### **Propiedades de un árbol binario**:

1. **Cada nodo tiene como máximo dos hijos**.
    
2. **Solo hay un camino desde la raíz hasta cualquier nodo**.
    
3. **No tiene ciclos**: No puedes volver al mismo nodo siguiendo las referencias de los hijos.
    

---

### **Tipos de árboles binarios**:

1. **Árbol binario común**: No tiene restricciones adicionales.
    
2. **Árbol binario de búsqueda (ABB)**:
    
    - Para cada nodo, todos los valores en el subárbol izquierdo son menores que el valor del nodo.
        
    - Todos los valores en el subárbol derecho son mayores que el valor del nodo.
        
3. **Árbol binario completo**:
    
    - Todos los niveles están completamente llenos, excepto posiblemente el último, que se llena de izquierda a derecha.
        
4. **Árbol binario perfecto**:
    
    - Todos los niveles están completamente llenos.
        
5. **Árbol binario balanceado**:
    
    - La altura de los subárboles izquierdo y derecho de cualquier nodo difiere en no más de 1.
        

---

### **Operaciones comunes en árboles binarios**:

1. **Inserción**: Añadir un nuevo nodo al árbol.
    
2. **Búsqueda**: Encontrar un nodo con un valor específico.
    
3. **Eliminación**: Eliminar un nodo del árbol.
    
4. **Recorridos**:
    
    - **Preorden**: Raíz → Izquierdo → Derecho.
        
    - **Inorden**: Izquierdo → Raíz → Derecho (útil para obtener los valores en orden en un ABB).
        
    - **Postorden**: Izquierdo → Derecho → Raíz.
        
    - **Por niveles**: Recorrer el árbol nivel por nivel (de arriba a abajo y de izquierda a derecha).
        

---

### **Ejemplo de un árbol binario**:

        10
       /  \
      5    15
     / \     \
    3   7     20

- **Raíz**: 10.
    
- **Hijos de 10**: 5 (izquierdo) y 15 (derecho).
    
- **Hojas**: 3, 7 y 20.
    

---

### **Aplicaciones de los árboles binarios**:

1. **Búsqueda eficiente**: En árboles binarios de búsqueda (ABB), la búsqueda tiene una complejidad de O(log⁡n)O(logn) en el mejor caso.
    
2. **Expresiones aritméticas**: Los árboles binarios se usan para representar y evaluar expresiones matemáticas.
    
3. **Árboles de decisión**: En inteligencia artificial y machine learning.
    
4. **Montículos (heaps)**: Estructuras usadas en algoritmos de ordenación y colas de prioridad.
    

---

En resumen, un **árbol binario** es una estructura de datos jerárquica y versátil que permite organizar y manipular información de manera eficiente. Es fundamental en algoritmos y aplicaciones de la informática.