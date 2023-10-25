## Configuration Script, 3 hours
***

*Will mainly be for Pi Picos*
- Pull MAC to use as a hardware token
	- Current issue without the Pico W; The regular Pico doesn't have a MAC, since it has no network hardware.
- Will need general location information
	- Room
	- Building
- Will configure at *least* cmakelists.txt, pins to be used when hooking up sensor
- ARP for Mac addies?

## False Positive Prevention, 3 Hours
***

*PIR sensors are prone to detecting false positives in changes in the environment such as sunlight, HVAC actions, and drafts. Using the US sensor along with the PIR will help avoid those false positives.*
- Use information gathered from initial setup to implement false detection prevention within the program
	- Will use readings from US sensor to determine if there was an object recently detected within the space
		- If yes, the reading from the PIR sensor will be read as valid, and the occupancy status will update
		- If not, the reading from the PIR sensor will be read as a false positive
	- The metric for the US sensor will be formed by an average of a large amount of readings (60 - 100), and that average will refresh over a certain interval (every half hour?)

## Switch for Office availability Override, 2 Hours
***
*Get feedback from Naseef on whether a switch would be better*
*This is for individual faculty members to be able to set their office as available/unavailable*

- Implement a callback to determine if the switch is reading high or low
## 


## Possible Issues
***
Github actions for code testing?