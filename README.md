# Dasar Pemrograman ES6

## Daftar Isi
1. [Pendahuluan](#pendahuluan)
2. [Let dan Const](#1-let-dan-const)
3. [Fungsi Panah (Arrow Functions)](#2-fungsi-panah-arrow-functions)
4. [Template Literals](#3-template-literals)
5. [Destructuring Assignment](#4-destructuring-assignment)
6. [Parameter Default](5-parameter-default)
7. [Operator Rest dan Spread](#6-operator-rest-dan-spread)
8. [Kelas (Class)](#7-kelas-class)
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

---

## 5. Parameter Default
```js
const suaraHewan = (hewan = "Serigala") => `${hewan} melolong di malam hari.`;
console.log(suaraHewan()); // Serigala melolong di malam hari.
console.log(suaraHewan("Rubah")); // Rubah melolong di malam hari.
```

---

## 6. Operator Rest dan Spread
### Spread Operator
```js
const hewanHutan = ["Harimau", "Ular", "Jaguar"];
const semuaHewan = ["Gajah", ...hewanHutan, "Rusa"];
console.log(semuaHewan);
```

### Rest Operator
```js
const deskripsiHewan = (pertama, ...lainnya) => {
  console.log(`Hewan pertama: ${pertama}`);
  console.log(`Hewan lainnya: ${lainnya.join(", ")}`);
};
deskripsiHewan("Macan Tutul", "Buaya", "Elang", "Beruang");
```

---

## 7. Kelas (Class)
```js
class Hewan {
  constructor(nama, habitat) {
    this.nama = nama;
    this.habitat = habitat;
  }
  deskripsi() {
    return `${this.nama} hidup di ${this.habitat}.`;
  }
}

const panda = new Hewan("Panda", "Hutan Bambu");
console.log(panda.deskripsi());
```

---

## 8. Modul
### Ekspor
```js
// file: hewan.js
export const burungHutan = "Beo";
export function terbang(hewan) {
  return `${hewan} sedang terbang tinggi!`;
}
```

### Impor
```js
// file: main.js
import { burungHutan, terbang } from "./hewan.js";
console.log(burungHutan); // Beo
console.log(terbang("Rajawali")); // Rajawali sedang terbang tinggi!
```

---

## 9. Promises dan Async/Await
### Promises
```js
const mencariMakanan = new Promise((resolve, reject) => {
  setTimeout(() => resolve("Beruang menemukan madu!"), 2000);
});

mencariMakanan.then((pesan) => console.log(pesan));
```

### Async/Await
```js
const mencariAir = async () => {
  return "Rusa menemukan sungai!";
};

mencariAir().then(console.log);
```

## 10. Map dan Set di ES6
### Map
```js
const kecepatanHewan = new Map();
kecepatanHewan.set("Cheetah", "Tercepat");
kecepatanHewan.set("Kura-kura", "Lambat");
console.log(kecepatanHewan.get("Cheetah")); // Tercepat
```

### Set
```js
const hewanUnik = new Set(["Serigala", "Rubah", "Serigala"]);
console.log(hewanUnik.size); // 2
```

---

## 11. Generator
```js
function* generatorHewan() {
  yield "Gajah";
  yield "Harimau";
  yield "Jerapah";
}

const hewan = generatorHewan();
console.log(hewan.next().value); // Gajah
console.log(hewan.next().value); // Harimau
console.log(hewan.next().value); // Jerapah
```
