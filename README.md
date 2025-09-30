timetable.html


<html>
<head>

</head>
<body style='background-image:linear-gradient(90deg,pink,blue);'>
    <style>
        th{
            background-color:black;
            color:white;
        }
        td{
            background-color:lightgrey;
        }
        caption{
            align-items: center;
            font-size: larger;
            border-width:5px;
            border-style:solid;
            border-color:black;
            color:black;
        }
    </style>
    <br>
    <br>

     
<center>
<table border="2" id="sta">
    <caption>Saveetha engineering college 
        TIME TABLE 
        Balaji T 25005672</caption>
   
        <tr>
            <th>Day/Time</th>
            <th>8-10</th>
            <th>10-12</th>
            <th>12-1</th>
            <th>1-3</th>
            <th>3-5</th>
            </tr>
        <tr>
            <th>Monday</th>
            <td>FWAD</td>
            <td>FREE SLOT</td>
            <td style="text-align: center;"><h3> L</h3></td>
            <td>Python</td>
            <td>FREE SLOT</td>
        </tr>
        <tr>
            <th>Tuesday</th>
            <td colspan="2">CE</td>
            <td style="text-align: center;"><h3> U</h3></td>
            <td colspan="2">FREE SLOT</td>
        </tr>
        <tr>
            <th>Wednesday</th>
            <td colspan="2">FWAD</td>
            <td style="text-align: center;"><h3> N</h3></td>
            <td>MENTOR MEET</td>
            <td>Python</td>
        </tr>
        <tr>
            <th>Thursday</th>
            <td>CE</td>
            <td>Python</td>
            <td style="text-align: center;"><h3> C</h3></td>
            <td>CE</td>
            <td>FCP</td>
            
        </tr>
        <tr>
            <th>Saturday</th>
            <td>CE</td>
            <td>FWAD</td>
        <td style="text-align: center;"><h3> H</h3></td>
        <td>CE</td>
        <td>FREE SLOT</td>
         </tr>
</table>
<br>
<br>
<br>
<table border="3" id="abc">
    <tr>
        <th>S.No</th>
        <th>Subject Code</th>
        <th>Subject Name</th>
    </tr>
    <tr>
        <td>1.</td>
    <td>19AI414</td>  
<td >Fundamental of Web Application Development(FWAD)</td>  </tr>
<tr>
    <td>2.</td>
    <td>19AI304</td>
    <td>Python</td>
</tr>
<tr>
    <td>3.</td>
    <td>19EN101</td>
    <td>Communicative English(CE)</td>
</tr>
</table>
</center>


</body>
</html>



views.py 

from django.shortcuts import render

# Create your views here.
def timetable(request):
    return render(request,'timetable.html')


urls.py



"""
URL configuration for pro project.

The `urlpatterns` list routes URLs to views. For more information please see:
    https://docs.djangoproject.com/en/5.2/topics/http/urls/
Examples:
Function views
    1. Add an import:  from my_app import views
    2. Add a URL to urlpatterns:  path('', views.home, name='home')
Class-based views
    1. Add an import:  from other_app.views import Home
    2. Add a URL to urlpatterns:  path('', Home.as_view(), name='home')
Including another URLconf
    1. Import the include() function: from django.urls import include, path
    2. Add a URL to urlpatterns:  path('blog/', include('blog.urls'))
"""
from django.contrib import admin
from django.urls import path
from app import views

urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.timetable)
]







