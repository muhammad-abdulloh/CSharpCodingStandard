## 0. O'zgaruvchilar

### 0.0 Nomlash
O'zgaruvchilarning nomlari ixcham bo'lishi va u o'ziga o'zlashtirgan qiymatni ma'nosini anglatuvchi bo'lishi kerak.
#### 0.0.0 Nomlash uslublari
##### Tavsiya etiladi
```cs
var student = new Student();
```
##### Tavsiya etilmaydi
```cs
var s = new Student();
```
##### Umuman tavsiya etilmaydi
```cs
var stdnt = new Student();
```

Xuddi shu qoida lambda ifodalari uchun ham amal qiladi.
##### Tavsiya etiladi
```cs
students.Where(student => student ... );
```
##### Tavsiya etilmaydi
```cs
studetns.Where(s => s ... );
```
<br />

#### 0.0.1 To'plamlarda nomlash uslublari
##### Tavsiya etiladi
```cs 
var students = new List<Student>();
```
##### Tavsiya etilmaydi
```cs
var studentList = new List<Student>();
```
<br />

#### 0.0.2 Nomga tipni elon qilish

##### Tavsiya etiladi
```cs
var student = new Student();
```
##### Tavsiya etilmaydi
```cs
var studentModel = new Student();
```
##### Umuman tavsiya etilmaydi
```cs
var studentObj = new Student();
```
<br />

#### 0.0.3 Null yoki Odatiy hol uchun nomlanish uslublari
Agar o'zgaruvchan qiymat odatiy bo'lsa, masalan ```int``` uchun ```0``` yoki ```string``` uchun ```null``` va siz bu qiymatni o'zgartirishni rejalashtiryapsiz (misol uchun sinash maqsadida) keyin nom ushbu qiymatni aniqlashi kerak.
##### Tavsiya etiladi
```cs
Student noStudent = null;
```
##### Tavsiya etilmaydi
```cs
Student student = null;
```
##### Doim tavsiya etiladi
```cs
int noChangeCount = 0;
```

##### Umuman tavsiya etilmaydi
```cs
int changeCount = 0;
```
<br /> <br />

### 0.1 O'zgaruvchilarni e'lon qilish
O'zgaruvchilarni e'lon qilish va uni instansiyalash, hatto qiymat keyinroq aniqlanishi kerak bo'lsa ham, o'zgaruvchining bevosita turini ko'rsatishi kerak.

#### 0.1.0 Aniq tiplar
Agar o'ng tomonning tipi **aniq bo'lmasa**, keyin o'zgaruvchingizni e'lon qilish uchun ```var``` dan foydalaning.
##### Tavsiya etiladi
```cs
var student = new Student();
```
##### Tavsiya etilmaydi
```cs
Student student = new Student();
````
<br />

#### 0.1.1 Aniq bo'lmagan tiplar
Qaytarilgan qiymat turining o'ng tomoni **aniq bo'lsa**, u holda siz o'z o'zgaruvchingizni uning turi bilan aniq e'lon qilishingiz kerak.
##### Tavsiya etiladi
```cs
Student student = GetStudent();
```
##### Tavsiya etilmaydi
```cs
var student = GetStudent();
```
<br />
