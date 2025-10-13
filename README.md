# Ex03 Time Table
# Date:13/10/2025
# AIM
To write a html webpage page to display your slot timetable.

# ALGORITHM
## STEP 1
Create a Django-admin Interface.

## STEP 2
Create a static folder and inert HTML code.

## STEP 3
Create a simple table using `<table>` tag in html.

## STEP 4
Add header row using `<th>` tag.

## STEP 5
Add your timetable using `<td>` tag.

## STEP 6
Execute the program using runserver command.

# PROGRAM

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
        


#views.py 

        from django.shortcuts import render

        def timetable(request):
            return render(request,'timetable.html')


#urls.py




    from django.contrib import admin
    from django.urls import path
    from app import views

    urlpatterns = [
    path('admin/', admin.site.urls),
    path('',views.timetable)
    ]


# OUTPUT

<img width="1920" height="971" alt="Screenshot 2025-09-28 004618" src="https://github.com/user-attachments/assets/65cf4dc1-3597-4b03-8402-1162d4aa7c7d" />



# RESULT
The program for creating slot timetable using basic HTML tags
