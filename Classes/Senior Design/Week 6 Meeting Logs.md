### Date: 10-4-2023, Meeting 5
***
- Ask Naseef for feeback on graph overview
- Look in to node red for MQTT  protocols
- Also need to look into mosquitto
- Admin/hardware users hitting endpoints need a valid Admin/hardware key to be able to hit certain points; Ex, hardware unit publishes to mqtt needs specific hardware key
	- We need this to avoid bad actors/spoofiing/etc.
	- Means more tables in  the database, how to relate users to roles?
		- Discord/Unix way, any set of perms can be based on an integer
- Talk through  situations of what user components we need
	- determines  endpoints we have within the API
- Some general srs feedback
- test.mosquitto.org

