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
* Parse the response body in json:
``` js
let jsonData = pm.response.json() 
```
* Check that the 1st element of the salary parameter is equal to salary*2 from request:
``` js
pm.test("Salary[1] is correct", function(){
    pm.expect(+jsonData.salary[1]).to.eql(+requestData.salary * 2)
});
``` 
* Write a loop that outputs the list items from the salary parameter to the console in order: 
``` js
for (i = 0; i<jsonData.salary.length; i++){
    console.log(`salary ${i}: ${jsonData.salary[i]}`);
} 
```
* Check that in the person parameter, the 1st element from u_name is equal to salary from request: 
``` js
pm.test("19: U_name element 1 = salary",function(){
    pm.expect(+jsonData.person.u_name[1]).to.eql(+requestData.salary)
});
```
* Write a loop that outputs the list items from the person parameter to the console in order: 
``` js
for (const property in jsonData.person) {
  console.log(`${property}: ${jsonData.person[property]}`);
} 
```

#### Continued in this file -> [HW 2](https://github.com/Saijentor/Postman/blob/main/HW%202.postman_collection.json)
<div align="center">
    <img src="https://res.cloudinary.com/postman/image/upload/t_team_logo/v1629869194/team/2893aede23f01bfcbd2319326bc96a6ed0524eba759745ed6d73405a3a8b67a8" width="70px"/>
</div>
