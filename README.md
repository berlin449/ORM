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

class Car(models.Model):
    car_name = models.CharField(max_length=100)        # Car name/model
    brand = models.CharField(max_length=100)           # Brand of the car
    year = models.IntegerField()                       # Manufacturing year
    price = models.DecimalField(max_digits=10, decimal_places=2)  # Price
    registration_number = models.CharField(max_length=50, unique=True)  # Unique car number

    def __str__(self):
        return f"{self.brand} {self.car_name} ({self.year})"


class CarAdmin(admin.ModelAdmin):
    list_display = ('car_name', 'brand', 'year', 'price', 'registration_number')



```

# OUTPUT
![alt text](<Screenshot 2025-09-22 201015.png>)

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
