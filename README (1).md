
create a database

```use emc```

create collection

```
db.createCollection("student");
```

insert record in collection 
```
db.student.insertMany([
    {
        enro: 102,
        fname: "Anish",
        lname: "Patel",
        city: "Valsad",
        gender: "M",
        contactno: "9632587410",
        dob: "06/01/2001"
    },
    {
        enro: 103,
        fname: "Kalp",
        lname: "Shah",
        city: "Baroda",
        gender: "M",
        contactno: "9630125874",
        dob: "13/10/2000"
    },
    {
        enro: 104,
        fname: "Yash",
        lname: "Bhakta",
        city: "Mumbai",
        gender: "M",
        contactno: "9987452103",
        dob: "08/05/2001"
    },
    {
        enro: 84,
        fname: "Aparana",
        lname: "Mukherjee",
        city: "Surat",
        gender: "F",
        contactno: "8563247890",
        dob: "26/06/2001"
    },
    {
        enro: 8,
        fname: "Arjun",
        lname: "Poduval",
        city: "Vapi",
        gender: "M",
        contactno: "8965230147",
        dob: "01/05/2001"
    },
    {
        enro: 105,
        fname: "Riya",
        lname: "Agrawal",
        city: "Navsari",
        gender: "F",
        contactno: "6985321470",
        dob: "02/09/2000"
    },
    {
        enro: 79,
        fname: "Monis",
        lname: "Khan",
        city: "Bardoli",
        gender: "M",
        contactno: "7895231053",
        dob: "23/11/2000"
    },
    {
        enro: 106,
        fname: "Abhishek",
        lname: "Choksi",
        city: "Surat",
        gender: "M",
        contactno: "6985327410",
        dob: "18/07/2001"
    },
    {
        enro: 49,
        fname: "Om",
        lname: "Patel",
        city: "Valsad",
        gender: "M",
        contactno: "9985632100",
        dob: "15/05/2001"
    },
    {
        enro: 20,
        fname: "Yash",
        lname: "Desai",
        city: "Surat",
        gender: "male",
        contactno: "9313100630",
        dob: "12/09/2000"
    }
]);
```

Perform the following operation on the collection:
1. Display all the documents of the collection.
find the all record in the collection 
```
db.student.find();
```
2. Show only the first name and last name of all the students.
```
db.student.find({},{fname:1,lname:1});
```
3. Display the list of unique cities of the students.
```
db.student.distinct("city")
```
4. Retrieve the student’s date of birth along with the student first name and last name.
```
db.student.find({},{fname:1,lname:1,dob:1})
```
5. Get all the details of students whose city is “Surat”
```
db.student.find({city:"Surat"})
```
6. Arrange all the documents of students in ascending order using “enro” number.
```
db.student.find().sort({enro:1});
```
7. Show the details of just the first five documents of the students.
```
db.student.find().limit(5)
```
8. Display only the details of last three documents of the students.
```
db.student.find().sort({enro:-1}).limit(3)
```
9. View the list of male students whose city is “Valsad”
```
db.student.find({gender:"M",city: "Valsad"})
```
10. Display all the documents in descending order.
```
 db.student.find().sort({enro:-1})
```
11. Display the list of first four students whose city is “Valsad” in order.
```
db.student.find({city: "Valsad"}).limit(4)
```
12. Update the contact number and date of birth of “Monis” to “6852987530” and“06/01/1999” respectively.
```
db.student.update({fname:"Monis"},{ $set:{ contactno:"6852987530",dob:"06/01/1999"}})
```
13. Find only the date of birth of “Om”.
14. Insert the document (100, Rohit, Mehera, Mumbai, 24/03/2003) in the collection.
15. Display the list of male students whose last name is “Patel”.
16. Insert the document (35, Priyank, Mistry, Anand, 18/06/2000, 9000800001) in the
collection.
17. Show all the details of student whose enrollment number is “102”.
18. Display the list of students whose gender in “NULL” or 0.
