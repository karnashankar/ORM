# Ex02 Django ORM Web Application
## Date: 04-04-2024

## AIM
To develop a Django application to store and retrieve data from a Football Players database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create 10 Football players

## PROGRAM
## Admin.py:
```
from django.contrib import admin
from.models import library,libraryAdmin
admin.site.register(library,libraryAdmin)
```

## models.py:
```
from django.db import models
from django.contrib import admin
class library(models.Model):
      serielno=models.IntegerField(primary_key=True);
      book_name=models.CharField(max_length=20);
      authorname=models.CharField(max_length=20);
      subject=models.CharField(max_length=50);
      publisher=models.CharField(max_length=10);
class libraryAdmin(admin.ModelAdmin):
      list_display=("serielno","book_name","authorname","subject","publisher");
```
## Urls.py:
```
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]
```
## Apps.py:
```
from django.apps import AppConfig


class OrmappConfig(AppConfig):
    default_auto_field = 'django.db.models.BigAutoField'
    name = 'ormapp'
```



admin.py
from django.contrib import admin
from .models import Employee,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)

models.py
from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.CharField(max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()

class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

```


## OUTPUT

![Screenshot 2024-04-04 152944](https://github.com/karnashankar/ORM/assets/121109150/f08efbde-1b73-4f50-a733-ebf563e995fa)




## RESULT
Thus the program for creating a database using ORM hass been executed successfully
