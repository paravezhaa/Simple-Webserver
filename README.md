# EX01 Developing a Simple Webserver
## Date:

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
admin.py
python
from django.contrib import admin
from .models import Product, ProductAdmin

admin.site.register(Product, ProductAdmin)

 models.py
python
from django.db import models
from django.contrib import admin

class Product(models.Model):
    product_id = models.CharField(max_length=20, primary_key=True)
    name = models.CharField(max_length=100)
    category = models.CharField(max_length=50)
    price = models.DecimalField(max_digits=10, decimal_places=2)
    rating = models.FloatField()
    seller = models.CharField(max_length=100)
    stock = models.IntegerField()
    offer = models.CharField(max_length=50, blank=True)
    delivery_date = models.DateField()

class ProductAdmin(admin.ModelAdmin):
    list_display = (
        'product_id',
        'name',
        'category',
        'price',
        'rating',
        'seller',
        'stock',
        'offer',
        'delivery_date',
    )

## OUTPUT:
<img width="1918" height="974" alt="EX 01" src="https://github.com/user-attachments/assets/cc32d21a-ff94-419f-9a01-ee509d7cb47a" />


## RESULT:
The program for implementing simple webserver is executed successfully.
