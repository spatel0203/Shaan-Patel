## Welcome to Shaan Patel's Website

Hello, my name is Shaan Patel. 

I am an aspiring software engineer self-teaching various programming languages like Python, HTML, CSS, and Javascript. Currently, I am learning web development utilizing HTML, CSS, and a Server-side JavaScript framework called Node.js!
```markdown
HERE IS A SAMPLE PROJECT I CREATED THAT UTILIZES AN APPLICATION PROGRAMMING INTERFACE FROM OPENWEATHERMAP.ORG TO GIVE A 5-DAY WEATHER FORECAST AT A SPECIFIC CITY AND COUNTRY

import json, sys, requests
from pprint import pprint

APPID = '7639e7c7731b03f0d7e502ef1918a99f'

#User Input - City and Country
if len(sys.argv) < 2:
    print('Usage: getOpenWeather.py city_name, 2-letter_country_code')
    sys.exit()
location = ','.join(sys.argv[1:4])

#API URL
url=f"http://api.openweathermap.org/data/2.5/forecast?q={location}&appid=7639e7c7731b03f0d7e502ef1918a99f"

#Downloads JSON File from API URL and checks user input
    response.raise_for_status()
except:
    raise Exception("Incorrect Location")
weatherData=json.loads(response.text)
w=weatherData["list"]

#Parse through JSON File and gather/print desired data
for i in range(0,40):
    if w[i]["dt_txt"][8:10] == w[i-1]["dt_txt"][8:10]:
        continue
    print(w[i]["dt_txt"] + ": ")
    print("\t" + "Description: " + w[i]["weather"][0]["description"])
    print("\t" + "Current Temp: " + str((w[i]["main"]["temp"]*1.8-459.67))[0:4] + " degrees Fahrenheit")
    print("\t" + "Feels Like: " + str((w[i]["main"]["feels_like"]*1.8-459.67))[0:4] + " degrees Fahrenheit")
    print("\t" + "Min Temp: " + str((w[i]["main"]["temp_min"]*1.8-459.67))[0:4] + " degrees Fahrenheit")
    print("\t" + "Max Temp: " + str((w[i]["main"]["temp_max"]*1.8-459.67))[0:4] + " degrees Fahrenheit")
```

### Contact

Email: Shaanp2258@gmail.com

### Thank You!

Thank you so much for viewing my website! It is currently in its developmental phase and will hold much more complex and developed 
aspects in the future!
