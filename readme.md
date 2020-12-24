
# Demo Web server REST API backend.

Written using the aiohttp framework.

## Functionality:

* http://localhost:8080/ :
     + GET request - answer - homepage(format html website).
* All requests below output the JSON data format.
* http://localhost:8080/students :
     + GET request- answer - data of all students stored in the database.
* http://localhost:8080/students/id :
     + GET request - answer - student data with the corresponding id.
     + POST request - answer - enters the data of the student with the given id into the database. Returns an error i
f this id is already in the database.
     + DELETE request - answer - deletes the student with the given id from the database.
     + PUT request - answer - changes the data of the student with the specified id in the database. If the student w
ith this id is not in the database adds it.

## Usage

* Run

Run STRICTLY from the directory where it is located main.py
```sh
python3 main.py
```
* Requests

Your data is in quotation marks " ".
```
curl -X GET -d http://0.0.0.0:8080/students
curl -X DELETE http://0.0.0.0:8080/students/id
curl -X POST -d 'name="your name"&surname="your surname"' http://0.0.0.0:8080/students/"id"
curl -X PUT -d 'surname="your name"&surname="your surname"' http://0.0.0.0:8080/students/"id"
```
You can also display the GET request in the browser by entering the appropriate address.
