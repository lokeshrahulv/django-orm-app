# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![image](https://user-images.githubusercontent.com/118423842/229407525-d946e196-d8f0-4fee-ac34-f82567d76d66.png)

## DESIGN STEPS

### STEP 1:
An Django application is created inside dataproject folder.

### STEP 2:
A python program is written to create a table to store and retrieve data.

### STEP 3:
The table is created with 6 fields in which the username field is made as PrimaryKey.

###step 4:
Then the project files migrated. A superuser is also created.

###step 5:
Now the server side program is executed .

###step 6:
The admin page of our website is accessed using username and password.

###step 7:
Records are added and saved in the table inside the database.

## PROGRAM
```
from django.db import models
from django.contrib import admin

class GitDatabase(models.Model):
    username_primary_key = models.CharField(max_length=30, help_text="User name must be unique", primary_key=True,unique=True)
    password = models.CharField(max_length=30)
    firstname = models.CharField(max_length=20)
    lastname = models.CharField(max_length=20)
    profile_photo = models.ImageField()
    email = models.EmailField(max_length=50,unique=True)

class GitAdmin(admin.ModelAdmin):
    list_display = ('username_primary_key', 'password', 'firstname', 'lastname','profile_photo','email')
```
## OUTPUT
![Screenshot (61)](https://user-images.githubusercontent.com/118423842/229406420-e60685e2-da72-4118-9dd6-9ee5d6db4583.png)
## RESULT
Thus a Django application is successfully developed to store and retrieve data from a database using Object Relational Mapping(ORM).
