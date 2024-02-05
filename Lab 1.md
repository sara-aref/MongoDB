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

Ans: ![UNFOUND](https://github.com/sara-aref/MongoDB/assets/147546807/6d086ba3-19dd-4f8f-85d4-204664f2ba1d)


### ● Try inserting many students using one insert statement.

Ans: ![UNFOUND](https://github.com/sara-aref/MongoDB/assets/147546807/ecb186ba-bd75-4648-9b05-079ac3461106)

![UNFOUND](https://github.com/sara-aref/MongoDB/assets/147546807/0f10a043-5e20-4e96-beb5-fa1cf1e5af5c)

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

### ● Students with Age more than or equal to 21, and their faculty isn't NULL.

Ans: 

### ● Display student with specific First Name, and display his First Name, Last name, IsFired fields only.

Ans:

### 5. Update the student with specific FirstName, and change his LastName.

Ans:

### 6. Delete Fired students.

Ans:

### 7. Delete all students collection.

Ans:

### 8. Delete the whole DB.

Ans:
