## CRUD operations
POST maps to Create
GET maps to Read
PUT maps to Update
DELETE maps to Delete (lol, duh)

### POST
POST is for actions which should have an impact every time they are executed, such as clicking a 'Buy' button. Information for a POST request is _not_ passed in the URL.

### GET
GET is _idempotent_; this means it can be repeated any number of times and will have the same impact as if it was only executed once. Information for a GET request is passed in the URL.

### PUT
PUT is also _idempotent_, meaning that it can be repeated any number of times and will have the same impact as if it was only executed once. It can also be used, like POST, to create entries.

