# The result of learning Postman is displayed in this repository:
_Contains two homework assignments._

## Postman [Homework 1](https://github.com/Saijentor/Postman/blob/main/Postman%20HW1.txt):

* __Method__: _POST_ 

    __EndPoint:__ `/user_info_3`
    
    __Request form data:__ 
             `name: str`
             `age: int`
             `salary: int`
        
```JSON
{
"name": "EP_2",
"request": {
    "method": "POST",
	"header": [],
	"body": {
	    "mode": "formdata",
	    "formdata": [
		    {
			    "key": "name",
			    "value": "Sergey",
			    "type": "text"
			},
			{
			    "key": "age",
			    "value": "27",
			    "type": "text"
			},
			{
			    "key": "salary",
			    "value": "3000",
			    "type": "text"
			}
		]
	},
	"url": {
	    "raw": "{{url}}:{{port}}/user_info_3",
	    "host": [
		    "{{url}}"
		],
	    "port": "{{port}}",
	    "path": [
		    "user_info_3"
		]
	}
},
"response": []
}
```

#### Continued in this file -> [HW 1](https://github.com/Saijentor/Postman/blob/main/HW%201.postman_collection.json)
***
## Postman [Homework 2](https://github.com/Saijentor/Postman/blob/main/Postman%20HW2.txt):
* Спарсить response body в json: 
``` js
let jsonData = pm.response.json() 
```
* Проверить, что 1-й элемент параметра salary равен salary*2 из request: 
``` js
pm.test("Salary[1] is correct", function(){
    pm.expect(+jsonData.salary[1]).to.eql(+requestData.salary * 2)
});
``` 
* Написать цикл который выведет в консоль по порядку элементы списка из параметра salary: 
``` js
for (i = 0; i<jsonData.salary.length; i++){
    console.log(`salary ${i}: ${jsonData.salary[i]}`);
} 
```
* Проверить, что в параметре person, 1-й элемент из u_name равен salary из request: 
``` js
pm.test("19: U_name element 1 = salary",function(){
    pm.expect(+jsonData.person.u_name[1]).to.eql(+requestData.salary)
});
```
* Написать цикл который выведет в консоль по порядку элементы списка из параметра person: 
``` js
for (const property in jsonData.person) {
  console.log(`${property}: ${jsonData.person[property]}`);
} 
```

#### Continued in this file -> [HW 2](https://github.com/Saijentor/Postman/blob/main/HW%202.postman_collection.json)
<div align="center">
    <img src="https://res.cloudinary.com/postman/image/upload/t_team_logo/v1629869194/team/2893aede23f01bfcbd2319326bc96a6ed0524eba759745ed6d73405a3a8b67a8" width="70px"/>
</div>
