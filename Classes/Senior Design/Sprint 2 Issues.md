## Configuration Script 2 hours
***
- Pull MAC to use as a hardware token identifier
- Will need general location information
	- Room
	- Building
- Will configure pins to be used for each sensor, as to make wiring easier
- Will install all necessary libraries

## Makefile, 2 hours
***
- Will build for 
	- testing rule
		- MQTT conections and transmssions
		- Hardware sensor programs
	- deployment rule
		- Build hardware programs for final deployment
## General Code Improvements, 1 hours
***
- Condense Hardware_output.cc to have a single us_measure function (or similarly named)
- Remove all CJSON library functions. 

## False Positive Prevention, 3 Hours
***
*PIR sensors are prone to detecting false positives in changes in the environment such as sunlight, HVAC actions, and drafts. Using the US sensor along with the PIR will help avoid those false positives.*
- Use information gathered from initial setup to implement false detection prevention within the program
	- Will use readings from US sensor to determine if there was an object recently detected within the space
		- If yes, the reading from the PIR sensor will be read as valid, and the occupancy status will update
		- If not, the reading from the PIR sensor will be read as a false positive
	- The metric for the US sensor will be formed by an average of a large amount of readings (60 - 100), and that average will refresh over a certain interval (every half hour?)
	- Reset US sensor initial average if the new readings are consistently much  larger (by around a meter or so) than the average.

## MQTT Broker Implementation, 4 hours
***
Secure port, dockerize the mqtt broker


## Possible Issues
***
Github actions for code testing?
MQTT BROKER BABYYYYYYY