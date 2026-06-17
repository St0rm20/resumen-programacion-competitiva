# Punteros en C++

## ¿Qué es un puntero?

Un puntero es una variable que almacena la **dirección de memoria** de otra variable.

Mientras una variable normal guarda un dato:

```cpp
int numero = 10;
```

un puntero guarda la ubicación donde ese dato se encuentra:

```cpp
int* ptr = &numero;
```

---

## Operadores importantes

### Obtener la dirección ; `&`

```cpp
int numero = 10;

cout << &numero;
```

Devuelve la dirección de memoria donde está almacenada la variable.

---

### Declarar un puntero ; `*`

```cpp
int* ptr;
```

Indica que `ptr` será un puntero a un entero.

---

### Acceder al valor apuntado ; `*`

```cpp
int numero = 10;

int* ptr = &numero;

cout << *ptr;
```

Salida:

```text
10
```

El operador `*` accede al contenido almacenado en la dirección guardada por el puntero.

---

## Relación entre variable y puntero

```cpp
int numero = 10;

int* ptr = &numero;
```

Supongamos que `numero` se almacena en la dirección `1000`.

| Expresión | Valor |
| --------- | ----- |
| `numero`  | 10    |
| `&numero` | 1000  |
| `ptr`     | 1000  |
| `*ptr`    | 10    |

---

## Representación visual

```text
numero
│
├── valor = 10
└── dirección = 1000


ptr
│
└── guarda 1000


*ptr
│
└── accede al valor almacenado en 1000
    resultado = 10
```

---

## Modificar una variable mediante un puntero

```cpp
int numero = 10;

int* ptr = &numero;

*ptr = 50;

cout << numero;
```

Salida:

```text
50
```

El cambio se realiza sobre la variable original, porque el puntero accede directamente a su dirección de memoria.

---

# ¿Por qué usar punteros?

## 1. Evitar copias innecesarias

En lugar de copiar un objeto grande, se puede pasar únicamente su dirección.

```cpp
void procesar(Jugador* jugador);
```

Copiar un puntero suele ocupar 8 bytes, independientemente del tamaño del objeto.

---

## 2. Modificar objetos originales

```cpp
void cambiar(int* x) {
    *x = 100;
}
```

```cpp
int a = 5;

cambiar(&a);
```

Después de la llamada:

```text
a = 100
```

---

## 3. Crear estructuras dinámicas

Los punteros permiten conectar objetos ubicados en diferentes posiciones de memoria.

Ejemplo:

```cpp
struct Node {
    int data;
    Node* next;
};
```

---

# Punteros en una lista enlazada

Cada nodo almacena:

* Un dato.
* Un puntero al siguiente nodo.

```text
head
 ↓
[10|•] → [20|•] → [30|NULL]
```

Equivalente a:

```cpp
struct Node {

    int data;

    Node* next;

    Node(int value) {

        data = value;

        next = nullptr;
    }
};
```

El campo `next` no guarda el siguiente nodo.

Guarda la dirección del siguiente nodo.

---

## Idea principal

```text
Variable normal
↓
Guarda datos

Puntero
↓
Guarda direcciones

*Puntero
↓
Accede al dato almacenado en esa dirección
```

La mayoría de las estructuras dinámicas en C++ se construyen a partir de esta idea; listas enlazadas, árboles, grafos y muchas implementaciones internas de la STL utilizan punteros para conectar objetos almacenados en memoria.


#Practica

https://leetcode.com/problems/reverse-linked-list/
