# 📚 JavaScript Array Methods – Guía Práctica

Este documento recopila **métodos nativos de JavaScript para trabajar con arrays**, con explicaciones claras y ejemplos prácticos.
Ideal para **pruebas técnicas, entrevistas y uso diario**.

---

## 🔁 Métodos de Iteración

### forEach

Ejecuta una función por cada elemento (no retorna nada).

```js
[1, 2, 3].forEach((n) => console.log(n));
```

### map

Transforma cada elemento y retorna un nuevo array.

```js
const result = [1, 2, 3].map((n) => n * 2);
// [2,4,6]
```

### filter

Filtra elementos según una condición.

```js
const evens = [1, 2, 3, 4].filter((n) => n % 2 === 0);
// [2,4]
```

### reduce

Reduce el array a un solo valor.

```js
const sum = [1, 2, 3].reduce((a, b) => a + b, 0);
// 6
```

---

## 🔍 Métodos de Búsqueda

### find

Devuelve el primer elemento que cumpla la condición.

```js
[5, 12, 8].find((n) => n > 10); // 12
```

### findIndex

Devuelve el índice del elemento encontrado.

```js
[5, 12, 8].findIndex((n) => n > 10); // 1
```

### includes

Verifica si un valor existe.

```js
[1, 2, 3].includes(2); // true
```

### indexOf / lastIndexOf

Busca la posición de un valor.

```js
[1, 2, 3, 2].indexOf(2); // 1
[1, 2, 3, 2].lastIndexOf(2); // 3
```

---

## ✂️ Métodos de Modificación

### push / pop

Agrega o elimina al final.

```js
const arr = [1, 2];
arr.push(3); // [1,2,3]
arr.pop(); // [1,2]
```

### shift / unshift

Agrega o elimina al inicio.

```js
arr.unshift(0); // [0,1,2]
arr.shift(); // [1,2]
```

### splice

Agrega, elimina o reemplaza elementos.

```js
const a = [1, 2, 3, 4];
a.splice(1, 2); // elimina [2,3]
```

---

## 🧩 Métodos de Copia y Unión

### concat

Une arrays.

```js
[1, 2].concat([3, 4]); // [1,2,3,4]
```

### slice

Copia una parte del array.

```js
[1, 2, 3, 4].slice(1, 3); // [2,3]
```

### spread (...)

Copia o combina arrays.

```js
const copy = [...[1, 2, 3]];
```

---

## 🔃 Métodos de Orden

### sort

Ordena elementos (⚠️ cuidado con números).

```js
[3, 1, 10].sort((a, b) => a - b); // [1,3,10]
```

### reverse

Invierte el array.

```js
[1, 2, 3].reverse(); // [3,2,1]
```

---

## 🧠 Métodos Avanzados

### some

Devuelve true si al menos uno cumple.

```js
[1, 2, 3].some((n) => n > 2); // true
```

### every

Devuelve true si todos cumplen.

```js
[1, 2, 3].every((n) => n > 0); // true
```

### flat

Aplana arrays.

```js
[1, [2, [3]]].flat(2); // [1,2,3]
```

### flatMap

Map + flat en uno.

```js
[1, 2, 3].flatMap((n) => [n, n * 2]);
```

---

## 🧪 Conversión

### Array.from

Convierte iterables en arrays.

```js
Array.from("ABC"); // ['A','B','C']
```

### Array.isArray

Verifica si es array.

```js
Array.isArray([]); // true
```

---

## 📌 Recomendaciones

- Prefiere `map`, `filter`, `reduce` sobre `for`
- Evita mutar arrays si trabajas con React/Vue
- Usa `slice` o spread para copias seguras

---

✍️ Autor: Juan Victor Bascope Castro  
🚀 Uso libre para aprendizaje y pruebas técnicas
