# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```md
To store and manipulate data for your application.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```md
model
```

In which part of the MVC pattern can we find C.R.U.D actions?

```md
controller
```

List at least 5 standard actions that C.R.U.D corresponds to?

```md
1. index
2. show
3. create
4. update
5. destroy
```

A user action fires a `PATCH` request for `pets/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list,
please include information on dynamic segments, the params hash and seralizers).

```md
1. The router receives the PATCH request for 'pets/1' and passes it on to the
   correct C.R.U.D. action in the controller based on the dynamic segments.
   C.R.U.D. actions are defined in the params hash in the controller.
2. The controller tells the model to make the change.
3. The model accesses the database to make the change
4. The database is altered (or fails) and the model generates a success or error message.
5. The model sends the success or error message to the client.
6. Depending on if the content that was changed is included in the serializer or not,
   the user will see the change represented in the browser.
```

What is the command to scaffold a `medicalRecords` join table which holds
refrences to a `pets` and a `vets` table?

```bash
rails g scaffold medicalRecords pets:references vets:references.
```

What is the point of having a join table?

```md
To allow many-to-many relationships.
```

Give an example of a one-to-many relationship and a many-to-many relationship:

```md
One primary care doctor can have many patients.
Many ingredients can be in many recipes.
```
