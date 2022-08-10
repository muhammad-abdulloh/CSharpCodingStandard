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

#### 0.1.0 Toza tiplar
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

#### 0.1.1 Yarim toza tiplar
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


#### 0.1.2 Toza bo'lmagan tiplar 
Qaytarilgan qiymat turining o'ng tomoni aniq va noma'lum bo'lsa (masalan, anonim turlar), o'zgaruvchi turi sifatida ```var``` dan foydalanishingiz mumkin.
##### Tavsiya etiladi
```cs
var student = new
{
    Name = "Muhammadabdulloh",
    Score = 100
};
```
<br /> <br />

### 0.2 Tashkillashtirish

#### 0.2.0 Sindirish
Agar o'zgaruvchilar deklaratsiyasi 120 belgidan oshsa, uni tenglik belgisidan boshlab ajrating(sindiring yoxud ikkinchi qatorga olib tushing).

##### Tavsiya etiladi
```cs
List<Student> washingtonSchoolsStudentsWithGrades = 
    await GetAllWashingtonSchoolsStudentsWithTheirGradesAsync();
```
##### Tavsiya etilmaydi
```cs
List<Student> washgintonSchoolsStudentsWithGrades = await GetAllWashingtonSchoolsStudentsWithTheirGradesAsync();
```
<br />

#### 0.2.1 Bir nechta deklaratsiyalar
Ikki yoki undan ortiq satrni egallagan deklaratsiyalar oldingi va keyingi oʻzgaruvchilar deklaratsiyasidan ajratish uchun ulardan oldin va keyin yangi qatorga ega boʻlishi kerak.

##### Tavsiya etiladi
```cs
Student student = GetStudent();

List<Student> washingtonSchoolsStudentsWithGrades = 
    await GetAllWashingtonSchoolsStudentsWithTheirGradesAsync();

School school = await GetSchoolAsync();
```

##### Tavsiya etilmaydi
```cs
Student student = GetStudent();
List<Student> washgintonSchoolsStudentsWithGrades = 
    await GetAllWashingtonSchoolsStudentsWithTheirGradesAsync();
School school = await GetSchoolAsync();
```
Bundan tashqari, faqat bitta satrdan iborat o'zgaruvchilar deklaratsiyasida ular orasida yangi qatorlar bo'lmasligi kerak.

##### Tavsiya etiladi
```cs
Student student = GetStudent();
School school = await GetSchoolAsync();
```

##### Tavsiya etilmaydi
```cs
Student student = GetStudent();

School school = await GetSchoolAsync();
```
<br />
