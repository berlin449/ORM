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
from .models import Car,CarAdmin
admin.site.register(Car,CarAdmin)
```
model.py
```
from django.db import models
from django.contrib import admin

class Car(models.Model):
    car_name = models.CharField(max_length=100)  
    brand = models.CharField(max_length=100)           
    year = models.IntegerField()                       
    price = models.DecimalField(max_digits=10, decimal_places=2)    
    speed=models.IntegerField()



class CarAdmin(admin.ModelAdmin):
    list_display = ('car_name', 'brand', 'year', 'price','speed')


```

# OUTPUT
<img width="1911" height="793" alt="Screenshot 2025-09-23 131627" src="https://github.com/user-attachments/assets/999f49a8-80a6-4964-aeb2-d03c41e26c8c" />



# RESULT
Thus the program for creating a database using ORM hass been executed successfully
