# Ex03 Time Table
## Date:08.10.25

## AIM
To write a html webpage page to display your slot timetable.

## ALGORITHM
### STEP 1
Create a Django-admin Interface.

### STEP 2
Create a static folder and inert HTML code.

### STEP 3
Create a simple table using ```<table>``` tag in html.

### STEP 4
Add header row using ```<th>``` tag.

### STEP 5
Add your timetable using ```<td>``` tag.

### STEP 6
Execute the program using runserver command.

## PROGRAM
```
 views.py
from django.shortcuts import render
from django.http import HttpResponse
def file1(request):
    return render(request,'time.html')


urls.py
from django.contrib import admin
from django.urls import path
from monaapp.views import file1
urlpatterns = [
    path('admin/', admin.site.urls),
    path('',file1),
]


<html>
    <head>
        <title>
            Timetable
        </title>
    </head>
    <body>
        {% load static %}

        <img src="{% static 'saveetha-engineering-college-(sriperumbudur)-chennai.png' %}" style="display:block; margin-left:auto; margin-right:auto; width=50%; height:auto;">
        <table border="1px" cellpadding="20px" cellspacing="3px" align="center" bgcolor="pink">
           <caption><b><i><centre>SLOT TIME TABLE-LEENA SHREE M (25018414)</centre></i></b></caption>
           <tr bgcolor=" baby pink">
               <th>DAY</th>
               <th>8-10</th> 
               <th>10-12</th>
               <th rowspan= "7" bgcolor="pink">LUNCH</th>
               <th>1-3</th>
               <th>3-5</th>
           </tr>
           <tr>
               <th>Monday</th>
               <td>-</td>
               <td>PYTHON</td>
               <td>PYTHON</td>
               <td>WEB</td>
           </tr>
           <tr>
               <th>Tuesday</th>
               <td>WEB</td>
               <td>ML</td>
               <td>PYTHON</td>
               <td>WEB</td>
           </tr>
           <tr>
               <th>Wednesday</th>
               <td>ML</td>
               <td>WEB</td>
               <td>MENTOR MEET</td>
               <td>ML</td>
           </tr>
           <tr>
               <th>Thursday</th>
               <td>ML</td>
               <td>-</td>
               <td>PYTHON</td>
               <td>PYTHON</td>
           </tr>
           <tr>
               <th>Friday</th>
               <td>WEB</td>
               <td>-</td>
               <td>-</td>
               <td>-</td>
           </tr>
           <tr>
               <th>Saturday</th>
               <td>-</td>
               <td>ML</td>
               <td>-</td>
               <td>-</td>
           </tr>
        </table>
    </body>
</html>
```
## OUTPUT

<img width="969" height="607" alt="{D949FA1F-48B2-477B-B782-3CBC0DD1B353}" src="https://github.com/user-attachments/assets/ca1c96ea-8bcb-4426-8c47-91b07d1759df" />

## RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
