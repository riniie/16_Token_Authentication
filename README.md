# Token Authentication

## How to create Token?
    1. Create Token manually in the admin 
    2. $ python manage.py drf_create_token username 
    3. $ http POST http://127.0.0.1:8000/gettoken/ username=username password=password 
    4. Using signals, automatically create token when a user is created. 


## How to send requests?

### GET Request
$ http GET http://127.0.0.1:8000/student/ 'Authorization: Token 0a5264c0a3515370557437c6f8adeb0f0dab6bd2' 
$ http GET http://127.0.0.1:8000/student/1/ 'Authorization: Token 0a5264c0a3515370557437c6f8adeb0f0dab6bd2'

### POST Request
$ http -f POST http://127.0.0.1:8000/student/ name=Isha roll=123 city=Bihar 'Authorization:Token 0a5264c0a3515370557437c6f8adeb0f0dab6bd2'

### PUT Request
$ http PUT http://127.0.0.1:8000/student/1/ name=Siya roll=123 city=LA 'Authorization:Token 0a5264c0a3515370557437c6f8adeb0f0dab6bd2'

### PATCH Request
$ http PATCH http://127.0.0.1:8000/student/1/ name=Shreya 'Authorization:Token 0a5264c0a3515370557437c6f8adeb0f0dab6bd2'

### DELETE Request
$ http DELETE http://127.0.0.1:8000/student/3/ 'Authorization:Token 0a5264c0a3515370557437c6f8adeb0f0dab6bd2'
