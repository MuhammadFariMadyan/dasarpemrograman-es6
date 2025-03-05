# Dasar Pemrograman ES6

## Daftar Isi
1. [Pendahuluan](#pendahuluan)
2. [Let dan Const](#let-dan-const)
3. [Fungsi Panah (Arrow Functions)](#fungsi-panah-arrow-functions)
4. [Template Literals](#template-literals)
5. [Destructuring Assignment](#destructuring-assignment)
6. [Parameter Default](#parameter-default)
7. [Operator Rest dan Spread](#operator-rest-dan-spread)
8. [Kelas (Class)](#kelas-class)
9. [Modul](#modul)
10. [Promises dan Async/Await](#promises-dan-asyncawait)
11. [Map dan Set di ES6](#map-dan-set-di-es6)
12. [Generator](#generator)
13. [Kesimpulan](#kesimpulan)

---

## Pendahuluan
Dasar pemrograman ES6 adalah ECMAScript 6, yaitu standar versi ke-6 dari bahasa pemrograman JavaScript. ES6 dirilis pada tahun 2015. ES6 membawa banyak fitur baru yang membuat JavaScript lebih mudah dan bersih untuk ditulis sehingga meningkatkan pengalaman pengembangan dan kinerja aplikasi JavaScript, terbukti dengan telah diadopsinya secara luas di seluruh komunitas pengembangan, bahkan kerangka kerja seperti React, Angular, dan Vue sangat bergantung pada fitur-fiturnya.

---

## 1. Let dan Const
### `let`
`let` memungkinkan deklarasi variabel dalam cakupan blok.
```js
let hewan = "Harimau";
hewan = "Gajah"; // Diizinkan
console.log(hewan); // Gajah
```

### `const`
`const` mendeklarasikan variabel konstan yang tidak dapat diubah.
```js
const rajaHutan = "Singa";
// rajaHutan = "Serigala"; // Error: Assignment to constant variable
console.log(rajaHutan);
```

---

## 2. Fungsi Panah (Arrow Functions)
Fungsi panah memberikan cara singkat untuk menulis fungsi.
```js
const mengaum = (hewan) => `${hewan} sedang mengaum!`;
console.log(mengaum("Beruang")); // Beruang sedang mengaum!
```

---

## 3. Template Literals
Template literals memungkinkan ekspresi dan string multiline.
```js
const hewan = "Rusa";
const pesan = `Si ${hewan} berlari cepat di dalam hutan.`;
console.log(pesan);
```

---

## 4. Destructuring Assignment
### Destructuring Array
```js
const hewanHutan = ["Monyet", "Macan", "Burung Hantu"];
const [pertama, kedua, ketiga] = hewanHutan;
console.log(pertama); // Monyet
console.log(kedua); // Macan
```

### Destructuring Object
```js
const burung = { nama: "Elang", kecepatan: "Cepat" };
const { nama, kecepatan } = burung;
console.log(nama); // Elang
console.log(kecepatan); // Cepat
```
