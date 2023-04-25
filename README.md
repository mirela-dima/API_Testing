# Api Testing Bugs Samples

Below are two Api Tests that i wrote during my course.

..........................

### The temperature doesn't adapt to the selected parameter.

**Test Data**

Endpoint: api.openweathermap.org/data/2.5/forecast?lat={lat}&lon={lon}&appid={API key}

lat=44.498955

lon=11.327591

appid= 32aef874fa3a01afd8c09e7945c5d479

units= metric  for Celsius

units= imperial  for Fahrenheit

**Description**

The data remains in standard units (temperature in Kelvin).

**Steps to reproduce**
1. Go to the the Postman tool and add a new GET request 
2. Paste the endpoint  
3. Add the latitude and the longitude parameters
4. Add the appid
5. Add units=metric 
6. Click on Send button
7. Cancel units=metric 
8. Add units=imperial
9. Click on Send button

**Expected results**

The temperature is displayed in Celsius/ Fahrenheit degrees.

**Actual results**

The temperature is displayed in Kelvin degrees.

.........................

### GET Weather in Bologna - languages

**Test Data**

Endpoint: api.openweathermap.org/data/2.5/forecast?lat={lat}&lon={lon}&appid={API key}

lat=44.498955

lon=11.327591

appid=32aef874fa3a01afd8c09e7945c5d479

lang=de

lang=ro

lang=it

**Description**

The words in the values are not in the selected language.

**Steps to reproduce**
1. Go to the the Postman tool and add a new GET request 
2. Paste the endpoint 
3. Add the latitude and the longitude parameters
4. Add the api key
5. Add lang=de
6. Click on Send button
7. Cancel lang=de
8. Add lang=ro
9. Click on Send button
10. Cancel lang=ro
11. Add lang=it
12. Click on Send button

**Expected results**

All the words in the values are correctly translated in the selected language.

**Actual results**

The words in the values are all in English.
