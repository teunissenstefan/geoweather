# Geoweather module for polybar
A simple weather module for polybar based on your the location of your current ip

![Preview](https://i.imgur.com/aSFXMbn.png)

## Requirements
  - python3
  - polybar
  - OpenWeatherMap API key
  - ipstack API key
## Usage
1. Install python3
2. Install poybar
3. Get a free OpenWeatherMap API key by registering https://home.openweathermap.org/users/sign_up
4. Get a free ipstack API key by registering at https://ipstack.com/product
5. Enter your API keys into geoweather.py
6. Add the module to your polybar bar
7. Reload polybar
## Arguments
Standard output will be celsius. Use -f for Fahrenheit and -k for Kelvin.

`geoweather.py -k`

`geoweather.py -f`
## Example module
```
[module/weather]
type = custom/script
interval = 600
format-prefix = " "
format = <label>
exec = python3 /path/to/geoweather.py
exec-if = ping openweathermap.org -c 1
format-underline = ${colors.primary}
```
