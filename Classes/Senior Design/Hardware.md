# Hardware
***
Welcome to the hardware section of the Room Availability Project. This directory serves as a comprehensive resource for all aspects related to the physical components and infrastructure of the project. We've organized this section into three primary subsections, each providing essential insights into the hardware aspect of the project.

## Functionality
The "Functionality" subsection offers a detailed exploration of the role and purpose of each hardware component within the Room Availability Project. Understanding the functionality of these components is vital for comprehending the project's architecture and how it achieves its objectives.

## Testing
In the "Testing" section, we delve into the critical topic of hardware testing. Here, we outline the methods and strategies employed to ensure the reliable operation of the hardware components & communication protocols. You'll find a comprehensive guide on how to verify the proper functioning of the hardware, identify potential issues, and validate that the system meets its intended performance standards.

## External Libraries & Sensors
The "External Libraries & Sensors" section provides an overview of the third-party libraries, software tools, and sensor technologies utilized in the project. These external components are crucial for the project's success, as they facilitate communication, data processing, and interaction with the hardware components. Here, we catalog and describe these external dependencies to help you understand their role in the system.

We encourage you to explore each of these subsections to gain a comprehensive understanding of the hardware aspects of the Room Availability Project. Whether you're a developer, a project stakeholder, or simply curious about the project's inner workings, this section will provide valuable insights into the hardware components and their significance within the project.


### Functionality
---

The hardware unit in the Room Availability Project serves a crucial role in collecting motion and distance information, which is then utilized for room occupancy detection on a per-room basis. The collected data undergoes logical operations to condense it into a single reading: either "detected" or "undetected occupancy." Subsequently, this reading is combined with other relevant data, and a consolidated payload is sent via MQTT to a centralized database for further analysis.

#### hardware_output.cc
The `hardware_output.cc` file is the heart of the hardware unit's functionality. This file contains the primary implementation of the program, orchestrating the collection of data, performing logical operations, and generating the occupancy status.

#### mqtt_test.cc
The `mqtt_test.cc` file is specifically designed to facilitate testing and validation of MQTT connections and publishing operations. It plays a critical role in ensuring the reliable transmission of occupancy status to the centralized database via MQTT.

#### hardware_test.cc
The `hardware_test.cc` file is dedicated to the testing of sensor readings, primarily for calibration purposes. This testing is crucial for fine-tuning and verifying the accuracy of the sensor data. It ensures that the hardware unit provides reliable and precise information, an essential component of the room availability detection system.

This section provides a comprehensive overview of the hardware unit's functionality, key files, and their respective roles within the Room Availability Project. Understanding the purpose of these components is essential for grasping how the hardware contributes to the overall success of the project.


### Testing
***
#### Manual Testing

In the realm of IoT projects, manual testing plays a pivotal role in ensuring the proper functioning and reliability of hardware components. Hardware, unlike software, often involves physical elements that cannot be fully validated through automated processes. Guidelines for testing hardware/communication components are listed below.

#### Sensor Testing

##### PIR Sensor Calibration

This project involves PIR (Passive Infrared) sensors. As such, it's crucial to calibrate them for accurate motion detection. Follow these steps to calibrate a PIR sensor:

1. **Environment Setup:** Ensure the test environment resembles the actual deployment environment as closely as possible.
    
2. **Power On:** Power on the PIR sensor.
    
3. **Calibration Period:** Give the PIR sensor time to calibrate. This process may take a few minutes during which the sensor "learns" the baseline or ambient environment.
    
4. **Test Movements:** Perform controlled movements within the sensor's field of view to ensure it detects motion accurately.
    
5. **Adjust Sensitivity:** Depending on your project's requirements, you might need to adjust the sensitivity of the PIR sensor. This can often be done using on-board potentiometers.
    
6. **Final Testing:** After calibration and sensitivity adjustments, thoroughly test the sensor with various scenarios to ensure it works as expected. Said scenarios may involve entering/exiting its view range at various distances, or remaining still within the view range and moving to test how it recognizes changes within an existing view.
    

##### Ultrasonic Sensor Considerations

For ultrasonic sensors, calibration is generally not required, as these sensors rely on measuring distance using sound waves and are inherently less susceptible to environmental factors affecting calibration.

#### MQTT Testing

MQTT (Message Queuing Telemetry Transport) is the communication protocol of this section of the project. An example of this test protocol is defined within mqtt_test.cc Here are the main functions of MQTT, and how you can test them:

1. **Broker Connection:** Ensure that your device is correctly connected to the MQTT broker server. Validate the server's URL, port, and security credentials.
    
2. **Topic Setup:** Define the MQTT topic to which you want to publish or subscribe. Make sure it aligns with your project's architecture.
    
3. **Test Publish:** Publish a sample message to the defined MQTT topic. Verify that the message is successfully transmitted to the broker.
    
4. **Test Subscribe:** Subscribe to the same MQTT topic and confirm that you receive the message you published earlier.
    
5. **Quality of Service (QoS):** Test MQTT messaging using different QoS levels to ensure message delivery reliability.
    
6. **Connectivity Loss:** Simulate connectivity loss between your device and the broker and verify that MQTT handles re-connection gracefully.
    

### External Libraries & Sensors
***
#### Libraries
pigpio
mosquittopp
make

#### Sensors
