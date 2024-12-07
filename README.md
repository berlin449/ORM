# Ex02 Django ORM Web Application
# Date:
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
![alt text](<Screenshot 2024-12-07 130326.png>)
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
models.py:

from django.db import models
from django.contrib import admin
class Electricity_Bill (models.Model):
    Customer_ID=models.CharField(max_length=20, primary_key=True)
    Customer_name=models.CharField(max_length=100)
    Bill_no=models.IntegerField(max_length=50)
    Bill_amount=models.IntegerField(max_length=20)
    Bill_date=models.DateField()

class Electricity_BillAdmin(admin.ModelAdmin):
    	list_display=('Customer_ID','Customer_name','Bill_no','Bill_amount','Bill_date')

admin.py:

from django.contrib import admin
from .models import Electricity_Bill, Electricity_BillAdmin
admin.site.register(Electricity_Bill, Electricity_BillAdmin)

# OUTPUT

![alt text](<Screenshot 2024-12-07 125032.png>)

![alt text](<Screenshot 2024-12-07 125047.png>)

# RESULT
Thus the program for creating a database using ORM hass been executed successfully
