# Data collector web UI #

Python Flask simple data collector service. Initially intended for uploading data from embedded projects like Arduino boards, ESP8266, ESP32,... 
Normally you can have sensor data like Temperature, Humidity, Moisture,... These will be displayed as graphic functions.
The other type of data are controll variables used to switch relays ON/OFF, so they are displayed as buttons.

## How to start ##
Istall Flask and plotly


    pip install Flask, plotly


Deploy it anywhere and go to url or IP address like 


    http://localhost:8000?key=AdminSecretKey123


The key can be changed at the top of the "main.py" file, just look for "ADMIN_KEY". 
To post new data go to:


     http://localhost:8000/postdata?key=AdminSecretKey123&N=data_name&V=data_value

     e.g. http://localhost:8000/postdata?key=AdminSecretKey123&N=Temperature&V=25.4
          http://localhost:8000/postdata?key=AdminSecretKey123&N=Humidity&V=30


You can use any HTML safe data_name and value. The timestamp will be automatically updated according to current time.
After posting few samples, you will be able to view a graphical display on the front page.

To set a control variable go to "/setvar" page. Also make sure you have the correct access key like:


    http://localhost:8000/setvar?key=AdminSecretKey123&N=var_name&V=var_value


To retrieve a control variable value, go to "/getvar" page like:


    http://localhost:8000/getvar?key=AdminSecretKey123&N=var_name


Control Variables are considered to be used for controlling relays, LED's,... which is why the home page displays them as buttons to be toggled.

## TODO ##

Add delete button so a data set can be cleared.

## Contact ##

* web: http://www.radinaradionica.com
* email: ujagaga@gmail.com

