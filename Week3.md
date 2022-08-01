# JavaScript Intermadate
## Array
Array adalah **tipe data** yang dapat menyimpan berbagai macam **tipe data** apapun didalamnya. Array didefinisikan atau menyimpan data di dalam *kurung siku* ([])
    
    Contoh Array
    let person = [
        name: "Raya"
        age: 18
        Taken: false
    ]
    console.log(person)
    outputnya akan berupa Raya, 18, taken: false

Array dihitung dari **index** data ke-0,

     let person = ["Raya", "Inda", "Fira", "Gina"]
       console.log(person[0])
     outputnya adalah Raya dan length(panjang) dari array adalah 4 dihitung mulai dari 0
     *melihat Panjang Array
     let panjangPerson = person.length
     console.log(panjangPerson)
     outputnya adalah 4

kita dapat mengupdate data pada array

     let person = ["Raya", "Inda", "Fira", "Gina"]
      person[0] = "Maya"
     console.log(person)
     outputnya adalah "Maya", "Inda", "Fira", "Gina"
     *update Jamak
     person = ['Ferdi', 'Adam', 'Farel', 'Aril']
     console.log(person)
     outputnya adalah 'Ferdi', 'Adam', 'Farel', 'Aril'

Array menggunakan Const kita tidak bisa mengubah array dengan array yang baru jika menggunakan Const

     const person = ["Raya", "Inda", "Fira", "Gina"]
     console.log(person)
     person[3] = "Mawar"
     console.log(person)
     output keduanya adalah "Raya", "Inda", "Fira" "Mawar"

Array Built-in Methods adalah **Method** yang dimiliki oleh **Array**, dengan built-in methods kita dimudahkan menggunakan **function/method umum** yang bisa kita gunakan. 
Contoh Built-in Methods
* .push() method untuk menambahkan item array pada urutan yang paling akhir

      Let no = []
      console.log(no)
      no.push(1,2,3)
      console.log(no)
      output keduanya adalah 1,2,3

* .pop() method untuk menghapus item array diurutan terakhir

      Let no = []
      console.log(no)
      no.push(1,2,3)
      console.log(no)
      no.pop()
      console.log(no)
      output ketiganya adalah 1,2

* .shift() method untuk menghapus item array index pertama

      let no = [1, 2, 3, 4, 5, 6]
       console.log(no)
      no.shift()
       console.log(no)
      Output keduanya adalah 2, 3, 4, 5, 6

* .unshift() method kebalikan dari .shift()

      let no = [2, 3, 4, 5, 6]
       console.log(no)
      no.unshift()
       console.log(no)
      Output keduanya adalah 1, 2, 3, 4, 5, 6

* .sort() method untuk mengurutkan dari terkecil ke terbesar
   
      let number = [1, 20, 0, 5, 13, 11];
      console.log(number);
      console.log(number.sort());
      outputnya adalah 0, 1, 5, 11, 13, 20

Perulangan Pada Array dapat menggunakan method **.map()** dan **.forEach()**
* .forEach() Method untuk melakukan perulangan pada setiap element array

      const num = [1, 2, 3, 4]
      num.forEach(Nom => {
      console.log(Nom)
      })
      outputnya adalah 1 2 3 4 secara vertikal

* .map() method untuk melakukan perulangan dengan membuat array baru

      let num = [1, 2, 3, 4]
      let nom = num.map(num => {
      return num * 3;
      })
      console.log(nom)
      outputnya adalah 3, 6, 9, 12


## Object
Object adalah sebuah **tipe data** pada variabel yang menyimpan **properti** dan **fungsi (method)**. **Properti** adalah sifat dari objek tersebut sedangkan **method** adalah apa yang menempel/yang bisa dilakukan oleh objek tersebut contohnya mobil propertinya adalah nama mobil, warna mobil sedangkan methodnya adalah rem, gas dan lain-lain.
  
     const Person = {
        name: 'Raya',
        Age: 18,
        taken: false
     } 
     console.log(Person)
     Output: name: 'Raya', Age: 18, taken: false

Memanggil Properti objek
    
     const Person = {
        name: 'Raya',
        Age: 18,
        taken: false
     } 
     console.log(Person.name) 
     *atau bisa juga 
     console.log(Person['name'])
     Output: Raya

Mengupdate Objek

      const Person = {
        name: 'Raya',
        Age: 18,
        taken: false
     } 
     Person.address = "Maluk, NTB"
     console.log(Person)
     Output: name: 'Raya', Age: 18, taken: false, address: "Maluk, NTB"

Menghapus properti Objek

     const Person = {
        name: 'Raya',
        Age: 18,
        taken: false
     } 
     delete Person.taken
     console.log(Person)
     Output: name: 'Raya', Age: 18

Method

     const Person = {
        name: function (){
            return "Raya"
        },
       age: function (){
        return 18
     }
     }
     console.log(Person.name())
     output: Raya

Nested Objek adalah objek yang bercabang atau objek yang berasal dari objek lain (turun menurun)

     const Student = {
        Student1: {
            name: "Raya",
            age: 18,
        }
        }
        console.log(Student.Student1)
        Output: name: "Raya", age: 18
       
Passed by reference adalah kita bisa mengubah data objek menggunakan function.

        let Person = {
        name: "Raya",
        age: 18
       };
      function change (obj) {
       obj.name = "Maya";
       obj.age = 17;
      }
      change(Person)
       console.log(Person)
       output: name: "Maya", age: 17

Looping Object 

      const Student = {
        Student1: {
            name: "Raya",
            age: 18,
        }
        for(let person in Student){
        console.log(Student[person]);
        }
        output: {name: "Raya", age: 18}

array of object digunakan untuk data yang lebih dari 1

       const Student = [
         {
            name: "Raya",
            age: 18,
        },
        {
            name: "Fira"
            age: 19,
        },
        {
            name: "Amira"
            age: 17,
        }
        ]
        student.forEach(listStudent) => {
            console.log(listStudent);
        }
        Output: {name: "Raya", age: 18}
                {name: "Fira", age: 19}
                {name: "Amira", age: 17}

## Recursive 
Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu.

        function countDown(number) {
        console.log(number);
        let nextNumber = number - 1;
  
       if (nextNumber > 0) {
        countDown(nextNumber);
       }
       }
       countDown(5);
       Output: 5 4 3 2 1
       Recursive akan berhenti memanggil dirinya sendiri jika kondisi terpenuhi

## Regex
Regex adalah susunan karakter yang dimana setiap karakter memiliki pola. Saat menggunakan Regex kita pasti membutuhkan pola(pattern). Untuk membuat polanya kita membutuhkan:
* Literals adalah kita membuat regex sesuai dengan text yang ingin kita cari/match atau mengandung text yang kita cari.

### Built-in Method
* test() mengembalikan nilai BOOLEAN (TRUE/FALSE) untuk kecocokan sebuat text yang dicari.

* karakter Set adalah kita menggunakannya untuk mencari min 1 karakter

* match() adalah method yang mengembalikan (karakter) nilai array dari karakter yang match.

* Flags
1. i = Untuk menghandle case-sensitive. Tidak mempermasalahkan besar kecilnya sebuah karakter. Tidak membedakan antara A dan a.
2. g = Untuk mencari kedalam seluruh string yang ingin dicari. Jika tidak menggunakan flags g, maka sistem akan mengembalikan nilai array pertama yang ditemukan saja atau tidak melanjutkan pencarian.

* Karakter set short syntax
1. \d : Seluruh number/digit character. Contohnya [ 0-9].
Negasi: TIDAK mengandung seluruh **number/digit character**.
2. \w : Alphanumeric character (26 huruf abjad dan angka). Contohnya [ A-Za-z0-9_].
Negasi:TIDAK mengandung **Alphanumeric character** (26 huruf abjad dan angka)
3. \s : Whitespace character (space, tab, newline, and similar). Contohnya [ \t\r\n\f\v]. Negasi:TIDAK mengandung **Whitespace character** (space, tab, newline, and similar)

* Quantifiers
adalah membuat format regex menjadi lebih baik dan rapih. Quantifiers bersifat **greedy**.

* Anchors
adalah kita ingin mencari karakter yang persis detail sama.

* Alternation
adalah membuat beberapa kalimat yang exactly sama persis dengan pencarian. menggunakan(|)

## OOP
Object Oriented Programming adalah suatu paradigma dalam pemrograman. OOP dapat diterapkan pada bahasa progrmming selain Javascript seperti **Ruby, Pyhton dan Java**,

### OOP pada Javascript
OOP dapat dibuat menggunakan **functon** dan **class**
* Function
     
      function Person(name, age){
        this.name = name;
        this.age = age;
        this.detail = function(){
            return `${this.name} berumur ${this.age}`;
        }
      }
      let person = new Person('Raya', 18);
      console.log(person.detail())
      output: Raya berumur 18

* class 

      class Person {
         constructor(name, age){
         this.name = name;
         this.age = age;
         }
          detail() {
            return `${this.name} berumur ${this.age}`;
         };
         };
       let person = new Person('Raya', 18);
       console.log(person.detail())
       Output: Raya berumur 18

This keyword adalah keyword khusus yang kembali pada objek pemiliknya. Maksudnya adalah nilai dari this sangat bergantung pada di mana keyword this ini di panggil.

4 pilar dalam OOP
* Encapsulation adalah cara untuk membatasi akses langsung ke properti atau method dari sebuah objek.

      function Pesawat (orang){
        const tiket = 400;
        this.orang = orang;
        this.harga = function(){
            return tiket * this.orang;
        }
      }
      let traveler1 = new Pesawat(2);
      traveler1.tiket = 600
      console.log(traveler.harga())
      output: 800

* Inheritance
adalah sebuah proses dimana sebuah class mewariskan property dan methodnya ke class lain atau childnya.
  
      class Person {
        constructor(name, age){
            this.name = name;
            this.age = age;
        };
        detail(){
            return `${this.name} berusia ${this.age}`;
        };
      };
      class orang extend Person {
        constructor(nme, age, address){
            super(name,age);
            this.address = address
        };
      };
      let client = new orang ('Raya', 18, 'Maluk');
      console.log(client)
      Output: orang {name: "Raya", age: 18, address: "Maluk", constructor: Object}

* Polymorpishm,
pada Polymorpishm, method yang diwariskan bisa kita ubah dengan behaviour yang berbeda menyesuaikan item yang kita buat.

         class people {
         transportasi(){
          console.log("Orang biasanya bekerja menggunakan kendaraan");
          }
          }
         class person extends people {
          transportasi(){
          console.log("Transportasi Umum");
          }
          }
         let Rudy = new person();
         Rudy.transportasi();
         output: Tranportasi Umum

* Abstraction adalah teknik untuk menyembunyikan detail tertentu dari sebuah objek dan hanya menampilkan funsionalitas atau fitur penting dari objek tersebut.

          class people {
         transportasi(){}
          }
         class person extends people {
          transportasi(){
          console.log("Transportasi Umum");
          }
          }
         let Rudy = new person();
         Rudy.transportasi();
         Output: Transportasi Umum


## Modules
Modules adalah code yang dapat di export dari suatu file javascript dan di import ke file javascript yang lain. Code disini adalah data yang dapat digunakan berulang kali.

Ada beberapa syarat untuk menjalankannya.
1. Harus menggunakan **static-server**
2. pada file html harus menambahkan script attribute type="modules"

## Web Storage
Web Storage adalah wadah untuk menyimpan data yang terikat pada browsernya. web yang sering digunakan oleh FE adalah
1. Local Storage menyimpan data selamanya selama data itu belum di hapus/di clear
2. Session Storage mempunyai API yang sama dengan Local Storage, hanya saja dia tidak menyimpan data selamanya, data akan terhapus bila browser yang dibuka tertutup.
3. IndexedDB datanya tidak berstruktur
4. Cookies (digunakan saat ada integeasi Back end) data akan tersimpan selama Back End belum menghapusnya

### API
API adalah singkatan dari *Application Programming Interface*, API adalah perantara lunak yang menyambungkan aplikasi untuk berbicara satu sama lain

## Asynchronous 
Asynchronous adalah teknik yang digunakan untuk membuat permasalah yang rumit dan dikerjakan dalam waktu lama menjadi mudah dan cepat terselesaikan dalam waktu singkat.

 ### Asynchronous Promise
   Asynchronous Promise digunakan untuk membuat perjanjian jika kondisi sudah terpenuhi maka dia mengembalikan nilainya. dan jika dia menginkar perjanjiannya maka kondisi dikembalikan ke kondisi yang tidak berhasil

         *cara mendeklarasikan Promise
         function GetUser(id) {
         return new Promise((resolve, reject) => {
          if (id !== "" && id !== undefined) {
          resolve(id);
         } else {
         reject("ID Harus di Isi");
          }
         });
         }

         *menggunakan Promise
         GetUser()
         .then((response) => {
           console.log(response);
         })
         .catch((error) => {
           console.log(error);
         });
         Output: ID Harus di isi











