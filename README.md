# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![image](https://github.com/Surendhar6/django-orm-app/assets/118352907/9c389cf8-4c9e-49b6-b4ce-1be93462b700)

## DESIGN STEPS

### STEP 1:
   Create a django application using django-admin startapp in command line. Head to the application directory created inside the project directory. Open the models.py file. In models.py create two classes one defining the attributes and the other one defining attribute value types.
### STEP 2:
   In the same directory, Head to admins.py and import the two classes from models.py that you have created earlier. Now register your created models in admins.py file and save both the files. 
### STEP 3:
   Start the Django server and head over to admin page. Using the admin interface, you can add or delete data.

## PROGRAM

### File: Models.py
```
from django.db import models
from django.contrib import admin
# Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email')
```

### File: Admin.py
```
from django.contrib import admin
from .models import Student,StudentAdmin
# Register your models here.
admin.site.register(Student,StudentAdmin)
```

## OUTPUT
![image](https://github.com/Surendhar6/django-orm-app/assets/118352907/4b02c11b-1466-4547-9298-596d9ad92cb7)

## RESULT
A Django application has been created that can be used to store and retrieve data from the database using Object Relational Mapping(ORM).
