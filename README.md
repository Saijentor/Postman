# The result of learning Postman is displayed in this repository:
_Contains two homework assignments._

## Postman Homework 1:

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

#### Continued in this file -> [Homework 1](https://github.com/Saijentor/Postman/blob/main/HW%201.postman_collection.json)

***

<div align="center">
    <img src="https://res.cloudinary.com/postman/image/upload/t_team_logo/v1629869194/team/2893aede23f01bfcbd2319326bc96a6ed0524eba759745ed6d73405a3a8b67a8" width="70px"/>
</div>
