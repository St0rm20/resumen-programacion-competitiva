# Cadenas

## 📌 1. Declaración e Inicialización
```
#include <iostream>
using namespace std;

string s1 = "Hola";       // Declaración estándar
string s2("Mundo");       // Otra forma de inicializar
string s3 = s1 + " " + s2; // Concatenación

```

## 📌 2. Obtener la Longitud de la Cadena

```
cout << "Longitud: " << s1.length() << "\n";  // También se puede usar s1.size()


```

## 📌 3. Obtener un Carácter en una Posición

```
cout << "Caracter en la posición 2: " << s1[2] << "\n";  
```

## 4. Buscar una Subcadena o Carácter

```
size_t pos = s1.find("la"); 
if (pos != string::npos) 
    cout << "Subcadena encontrada en: " << pos << "\n";
else 
    cout << "No encontrada\n";
```

Buscar desde una posición específica:

`size_t pos2 = s1.find('o', 1);  // Buscar 'o' a partir del índice 1 `




![image](https://github.com/user-attachments/assets/f34788f6-194e-43ac-8437-62089d6e6800)
