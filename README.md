# Ex02 Django ORM Web Application
# Date:22-09-2025
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM:
admin.py
```
from django.contrib import admin
from .models import Student, StudentAdmin
admin.site.register(Student,StudentAdmin)
```
model.py
```
from django.db import models
from django.contrib import admin

class Student(models.Model):
    name = models.CharField(max_length=100)      # student name
    roll_no = models.IntegerField(unique=True)   # roll number
    age = models.IntegerField()                  # age
    email = models.EmailField(unique=True)       # email
    date_of_birth = models.DateField()           # date of birth

class StudentAdmin(admin.ModelAdmin):
        list_display=('name','roll_no','age','email','date_of_birth')


```

# OUTPUT
![alt text](<Screenshot 2025-09-22 201015.png>)

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
