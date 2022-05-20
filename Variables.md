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

#### 0.0.2 Tiplarning nomlanish uslublari

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



