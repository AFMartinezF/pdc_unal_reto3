# Reto 3 

En este repositorio se muestra un pseudocódigo para obtener los números primos hasta n

```pseudocode
[variables]
  primos : lista de enteros
  n : entero
  i, j : enteros

primos := []
i := 2

Mientras (i <= n) hacer
  es_primo := verdadero
  j := 2
  Mientras (j * j <= i) hacer
    Si modulo(i, j) == 0
      Entonces es_primo := falso
      Romper
    sino
      j := j + 1
  Fin mientras
  Si es_primo
    Entonces añadir i a la lista de primos
  i := i + 1
Fin mientras
```

La representación gráfica de este algoritmo usando un diagrama de flujo se muestra a continuación

```mermaid
flowchart TD;
    A([Inicio]) --> B[Ingresar el valor de  n];
    B --> C;
    C[Declarar i=2];
    C--> D;
    D{i es menor o igual que n?} -- Sí --> E;
    E[Declarar es_primo verdadero y j = 2];
    E --> F;
    F{j*j es menor o igual que i?} -- Sí --> G[Calcular i modulo j];
    G --> H;
    H{El módulo es 0?} -- Sí --> I[Declarar es_primo falso];
    I --> K;
    H -- No -->J[j=j+1] --> F;
    F -- No --> K{es_primo?} -- Sí -->L[Añadir i a la lista de primos]
    L --> M[i = i+1];
    K -- No --> M;
    M --> D;
    D -- No --> Z([Fin programa]);
```
