# Lab5_202001255
# IT314 -Software Engineering
# Static Analysis

git repository: https://github.com/jassics/learning-python/blob/master/exercises

Language: Python

Tool:mypy/mypy Playground
<h1>1)
<h1>Code:</h1>

#!/usr/bin/python3


  num = int(input('Enter a number: '))
<br>except:
    <br>exit("Only integer please!")
<br>if num < 0:
    <br>exit('Number should be positive')
<br>else:
    <br>for prime in range(2, num):
        <br>if (num % prime)= 0:
            <br>print(num, 'is not a prime number')
            <br>break
    <br>else:
        <br>print(num, 'is a prime number')
        
 <h1>Error: </h1>
 
 
![c1](https://user-images.githubusercontent.com/96589841/227475600-a89bc858-3d28-496f-9dfb-353ae34ff3f1.PNG)

<h1>2)
<h1>Code:</h1>

#!/usr/bin/python3

<br>def fahr_to_cel(fahrenheit):
    <br>celsius = (fahrenheit - 32) / 1.8
    <br>return celsius
<br>try:
    <br>fahr = int(input('Enter temperature in Fahrenheit please: '))
<br>except:
    <br>exit("I am sorry. Only real numbers are allowed")
<br>print(fahr_to_cel())

 <h1>Error: </h1>
 
 ![c2](https://user-images.githubusercontent.com/96589841/227477371-e2e1475b-df3f-42ae-96a4-f4643166da34.PNG)


<h1>3)
<h1>Code:</h1>

#!/usr/bin/python

<br>try:
    <br>lower = int(input('Enter start range: '))
    <br>upper = int(input('Enter end range: '))
<br>except:
    <br>exit("Make sure ranges are integers only")
<br>if( lower < 0 or upper < 0 ):
    <br>exit("Ranges must be positive numbers")
<br>print("Prime numbers between", lower, "and", upper, "are:")
<br>for num in range(lower, upper+1):
    <br>if(num > 1):
        <br>for i in range(2, num)
            <br>if (num % i) == 0:
                <br>break
        <br>else:
            <br>print(num)
   
 <h1>Error: </h1>
 
 ![c3](https://user-images.githubusercontent.com/96589841/227478628-f1c99855-0b31-4ee0-9f62-3d2d057ba911.PNG)
 
<h1>4)
<h1>Code:</h1>

 #!/usr/bin/python

<br>num_list = [2, 1, 3, 5, 6, 11, 2, 13, 4, 15]
<br>target = 12
<br>def twoSum(arr, t):
    <br>index_dict = {}
    <br>length = len(arr)
    <br>index = 0
 <br>while index < length:
        <br>if (t - arr[index]) in index_dict:
            <br>return index_dict[t - arr[index]], index
        <br>index_dict[arr[index]] = index
        <br>index += 1
<br>print(twoSum(num_list, target))

 <h1>Error: </h1>
 
![c4](https://user-images.githubusercontent.com/96589841/227482584-13af2687-66bc-439f-b013-55556d705e23.PNG)

<h1>5)
<h1>Code:</h1>


#!/usr/bin/python3
<br>#import requests
<br>import json
<br>from datetime import datetime

<br>def time_from_utc_with_timezone(utc_with_tz):
    <br>local_time = datetime.utcfromtimestamp(utc_with_tz)
    <br>return local_time.time()

<br>api_key = ""
<br>city_name = input("Enter city name : ")
<br>weather_url = 'http://api.openweathermap.org/data/2.5/weather?q=' + city_name + '&appid='+api_key
<br>response = requests.get(weather_url)
<br>weather_data = response.json()

<br>if weather_data['cod'] == 200:
    <br>kelvin = 273.15 # Temperature shown here is in Kelvin and I will show in Celsius
    <br>temp = int(weather_data['main']['temp'] - kelvin)
    <br>sunrise = weather_data['sys']['sunrise']
    <br>sunset = weather_data['sys']['sunset']
    <br>timezone = weather_data['timezone']
    <br>cloudy = weather_data['clouds']['all']
    <br>sunrise_time = time_from_utc_with_timezone(sunrise + timezone)
    <br>sunset_time = time_from_utc_with_timezone(sunset + timezone)
    <br>print(f"Weather Information for City: {city_name}")
    <br>print(f"Temperature (Celsius): {temp}")
    <br>print(f"Sunrise at {sunrise_time} and Sunset at {sunset_time}")
    <br>print(f"Cloud: {cloudy}%")
<br>else:
    <br>print(f"City Name: {city_name} was not found!")
 
 <h1>Error: </h1>
 
 ![c5](https://user-images.githubusercontent.com/96589841/227489068-0528c6ef-18b0-420d-9a64-1592de71e119.PNG)
