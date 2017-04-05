# study-rest
RestfulAPI with Python and Flask, see this [article](https://blog.miguelgrinberg.com/post/designing-a-restful-api-with-python-and-flask) for more information. 

The HTTP request methods are typically designed to affect a given resource in standard ways:

| HTTP Method | Action | Examples | 
|-------------|--------|----------|
| GET |  Obtain information about a resource | http://example.com/api/orders (retrieve order list) | 
| GET | Obtain information about a resource | http://example.com/api/orders/123 (retrieve order #123) | 
| POST | Create a new resource | http://example.com/api/orders (create a new order, from data provided with the request) |
| PUT | Update a resource | http://example.com/api/orders/123 (update order #123, from data provided with the request) |  
| DELETE | Delete a resource | http://example.com/api/orders/123 (delete order #123) | 

The task of designing a web service or API that adheres to the REST guidelines then becomes an exercise in identifying the resources that will be exposed and how they will be affected by the different request methods.

Our tasks resource will use HTTP methods as follows:

| HTTP Method | URI | Action | 
|-------------|-----|--------|
| GET | http://[hostname]/todo/api/v1.0/tasks | Retrieve list of tasks | 
| GET | http://[hostname]/todo/api/v1.0/tasks/[task_id] | Retrieve a task | 
| POST | http://[hostname]/todo/api/v1.0/tasks | Create a new task | 
| PUT | http://[hostname]/todo/api/v1.0/tasks/[task_id] | Retrieve list of tasks | 
| DELETE | http://[hostname]/todo/api/v1.0/tasks/[task_id] | Delete a task | 

To start the server, run
```
cd todo-api && chmod +x app.py && ./app.py
```
And test is via
```
curl -u evgeny:python -i http://localhost:5000/todo/api/v1.0/task
```
