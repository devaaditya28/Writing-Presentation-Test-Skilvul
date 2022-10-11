# **Writing Test - Week 4**

## _Async-Await_

### Definisi

Selain menggunakan _callback_ dan _promise_, kita juga bisa menggunakan async/await untuk menggunakan _asynchronous_ pada JavaScript. _Async/await_ baru ada ketika update _ES8_ JavaScript dan dibangun menggunakan _promise_. Jadi sebenarnya _async/await_ dan _promise_ itu sama saja, namun hanya berbeda dari syntax dan cara penggunaannya.

Ada 2 kata kunci yang memiliki pengertian sebagai berikut:

- _async_, mengubah function _synchronous_ menjadi _asynchronous_.
- _await_, menunda eksekusi hingga proses _asynchronous_ selesai.

Sebuah _async function_ bisa tidak berisi _await_ sama sekali atau lebih dari satu _await_. Keyword _await_ hanya bisa digunakan didalam _async function_, jika digunakan di luar _async function_ maka akan terjadi error.

### _Async_

```h
// async menggunakan keyword function 
async function tesAsyncAwait() {
  return "Fulfilled";
}

console.log(tesAsyncAwait());
```

```h
// async menggunakan arrow function
const tesAsyncAwait = async () => {
  return "Fulfilled";
};

console.log(tesAsyncAwait());
```

![async-function](img/async-function.png)

### _Await_

_await_ hanya bisa digunakan dalam _async function_ dan _await_ adalah keyword dalam _async_ yang digunakan untuk menunda hingga proses _asynchronous_ selesai.

Syntax :

```h
async function tesAsyncAwait() {
   await 'Fulfilled';
}
```

Kita juga bisa memberikan _error handling_ pada _async/await_. Contoh penggunaan _async/await_ :

```h
// membuat promise
let nonton = (kondisi) => {
    return new Promise((resolve, reject) => {
      if (kondisi == "jalan") {
        resolve("nonton terpenuhi")
      }
      reject("batal nonton")
    })
}

// buat async function
async function asyncNonton() {
    try {
        let result = await nonton("jalan")    
        console.log(result);
    } catch (error) {
        console.log(error);
    }
}
asyncNonton()
```

![async-await](img/async-await.png)

Menggunakan _promise_ biasa (then catch) :

```h
// membuat promise
let nonton = (kondisi) => {
    return new Promise((resolve, reject) => {
      if (kondisi == "jalan") {
        resolve("nonton terpenuhi")
      }
      reject("batal nonton")
    })
}

// then catch
nonton("tidur")
.then(result => {
    console.log(result);
}).catch(error => {
    console.log(error);
})
```

![asyn-await-error](img/async-await-error.png)

## _Fetch_

Dalam JavaScript kita bisa mengirimkan _network request_ dan juga bisa mengambil informasi data terbaru dari server jika dibutuhkan.

Contoh _network request_ yang bisa dilakukan :

- Mengirimkan data dari sebuah _form_.
- Mengambil data untuk ditampilkan dalam _list/table_.
- Mendapatkan notifikasi.

Dalam melakukan _network request_, JavaScript memiliki metode bernama `fetch()`.

Proses melakukan `fetch()` adalah salah satu proses _asynchronous_ di JavaScript sehingga kita perlu menggunakan salah satu diantara _promise_ atau _async/await_.

_fetch_ dengan _promise_ :

```h
fetch("https://digimon-api.vercel.app/api/digimon")
.then(result => {
    console.log(result);
    return result.json()
})
.then(result => {
    console.log(result);
})
.catch(error => {
    console.log(error);
})
```

![fetch-promise](img/fetch-promise.png)

_fetch_ dengan _async-await_ :

```h
let getDataDigimon = async () => {
    let response = await fetch("https://digimon-api.vercel.app/api/digimon")
    let result = await response.json()
    console.log(result);
}
getDataDigimon()
```

![fetch-async-await](img/fetch-async-await.png)

_fetch_ data di internet dan menambahkan _DOM_ :

```h
let containerDigimon = document.getElementById("list-digimon")

let getDataDigimon = async () => {
    let response = await fetch("https://digimon-api.vercel.app/api/digimon")
    let digimons = await response.json()
    
    digimons.slice(0, 5).forEach((item, index) => {
        containerDigimon.innerHTML += 
        `<div>
        <img src="${item.img}" alt="digimons" width="70" />
        <h3>${item.name}</h3>
        </div>`

        console.log(item);
    })
}
getDataDigimon()
```

![fetch-dom](img/fecth-dom.png)