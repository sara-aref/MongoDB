### Lab 1

### 1. Create database named: FacultySystemDB.

Ans: use FacultySystemDB

### 2. Create collection (student) that has:
### ● FirstName: string, LastName: string, Age: Number, Faculty: An object that	has Name and Address
### ● Grades: An array of objects, each object has: CourseName, Grade, Pass (Boolean).
### ● IsFired: Boolean

Ans: db.createCollection("student")

### 3. Insert 3 (at least) documents in Student collection with different values.
### ● Try inserting one record each time

Ans: ![UNFOUND](https://github.com/sara-aref/MongoDB/assets/147546807/354a0042-b3a4-42b5-8ac0-0664141cb9ff)

### ● Try inserting many students using one insert statement.

Ans: ![UNFOUND](https://github.com/sara-aref/MongoDB/assets/147546807/0b4f6a50-24fc-4a7b-8bae-87a9300f6ca4)

### 4. Retrieve the following data:
### ● All Students.

Ans: db.student.find({})

### ● Student with specific First Name.

Ans: db.student.find({"firstName" : "Sara"})

![UNFOUND](https://github.com/sara-aref/MongoDB/assets/147546807/fdb0239a-0717-473c-90e8-60f711a125ac)

### ● Students who his First Name=Ahmed, or Last Name= Ahmed.

Ans: db.student.find({$or: [{"firstName" : "Shimaa"}, {"lastName" : "Alaa"}]})
![UNFOUND](https://github.com/sara-aref/MongoDB/assets/147546807/8ab92a07-3717-4c4e-a46d-489d704943bf)

### ● Students that their First name isn't "Ahmed".

Ans: db.student.find({"firstName" : {$ne : "Sara"}})

![UNFOUND](https://github.com/sara-aref/MongoDB/assets/147546807/77669524-d1e0-467a-841e-4daf23751d2e)

![UNFOUND](https://github.com/sara-aref/MongoDB/assets/147546807/e7e410a8-3f68-4b95-8d26-8964d97faf0d)

### ● Students with Age more than or equal to 21, and their faculty isn't NULL.

Ans: db.student.find({$and : [{"age" : { $gte : 21}}, {"faculty" : {$ne : null}}]})

### ● Display student with specific First Name, and display his First Name, Last name, IsFired fields only.

Ans: db.student.find({"firstName" : "Hadeer"}, {"firstName" : 1, "lastName" : 1, "IsFired" : 1, "_id" : 0})

![UNFOUND](https://github.com/sara-aref/MongoDB/assets/147546807/448fab6f-6476-4737-abf0-9aa37abf6a23)

### 5. Update the student with specific FirstName, and change his LastName.

Ans: db.student.updateOne({"firstName" : "Sara"} , {$set : {"lastName" : "Hassan"}})

### 6. Delete Fired students.

Ans: db.student.deleteMany({"IsFired" : true})

### 7. Delete all students collection.

Ans: db.student.drop()

### 8. Delete the whole DB.

Ans: db.dropDatabase()
