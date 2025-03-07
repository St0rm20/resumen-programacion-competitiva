
Estructura del archivo
```
// 📂 1. Inclusión de librerías necesarias
#include <bits/stdc++.h>
// 📂 2. Uso de un namespace (opcional, pero útil en competencias)
using namespace std;

// 📂 3. Método para optimizar la entrada y salida
#define fastIO() ios_base::sync_with_stdio(0); cin.tie(0);

// 📂 4. Métodos auxiliares para el problema
int suma(int a, int b) {
    return a + b;
}

// 📂 5. Función principal (Main)
int main() {
    fastIO(); // Optimización de entrada/salida

    int x, y;
    cin >> x >> y;

    cout << "La suma es: " << suma(x, y) << "\n";

    return 0;
}
```
Recomendaciones
Usar como space name std, ahorra tiempo al definir la entrada y salida de datos, dejarlo justo debajo de los llamados a las librerías:
 using namespace std;

Librerías
En este caso se recomienda usar la librería bits/stc++.h, ya que incluye la mayoría de librerías estándar tales como:
📂 Librerías de Entrada/Salida

<iostream> → Entrada y salida estándar (cin, cout).

<cstdio> → Entrada/salida en estilo C (printf, scanf).

<iomanip> → Manipulación de la salida (setprecision, fixed).

📂 Librerías de Contenedores STL

<vector> → Arreglos dinámicos.

<deque> → Cola de dos extremos.

<list> → Lista doblemente enlazada.

<queue> → Cola FIFO (queue) y cola de prioridad (priority_queue).

<stack> → Pila LIFO (stack).

<set> → Conjunto ordenado (set y multiset).

<map> → Diccionario clave-valor (map y multimap).

<unordered_set> → Conjunto desordenado.

<unordered_map> → Diccionario clave-valor sin orden.

📂 Librerías de Algoritmos

<algorithm> → Algoritmos generales (sort, binary_search, max_element).

<functional> → Funciones (greater<int>, less<int>).

<numeric> → Funciones matemáticas (accumulate, gcd, lcm).

📂 Librerías de Cadenas
<string> → Manejo de cadenas (string).
<cstring> → Funciones de manipulación de char* (memset, strcpy, strcmp).
📂 Librerías de Matemáticas
<cmath> → Funciones matemáticas (sqrt, pow, log, abs).
<cstdlib> → General (rand, abs, atoi).
<ctime> → Tiempo (time, clock).
<climits> → Constantes de enteros (INT_MAX, LLONG_MIN).
<cfloat> → Constantes de flotantes (DBL_MAX, FLT_MIN).
<cassert> → Aserciones (assert para depuración).
📂 Otras librerías útiles
<bitset> → Manipulación eficiente de bits.
<tuple> → Tuplas (std::tuple).
<utility> → Funciones auxiliares (pair, make_pair, swap).
<random> → Generación de números aleatorios.
<chrono> → Medición de tiempo (high_resolution_clock).
<thread> → Manejo de hilos.
<mutex> → Sincronización de hilos.
Las poderosas ios_base::sync_with_stdio(0); y cin.tie(0);, deben ser las primeras instrucciones dentro del main ya que optimizan la lectura e impresión de C++, lo cual se ve reflejado en ahorro de tiempo de ejecución =)
Finalmente (y en resumen) el esqueleto de un programa queda así




Links de la información:
https://github.com/CPCESFM/Material-Apoyo-Tutoriales/blob/master/comenzando/

