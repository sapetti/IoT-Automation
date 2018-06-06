# IoT-Automation
The aim of this project will allow manage boards such as NodeMCU or Arduino from a cloud platform and retrieve data from them.

## Edge
In an initial stage it will only do the following tasks:
* Register: Once the board is connected to internet.
* Input/Output: The board will read/write data through the GPIO.

__Technologies__
* [Builds](https://nodemcu-build.com/)
* [ESPlorer](https://esp8266.ru/esplorer/)
* [Esptool](https://github.com/espressif/esptool)
* [NodeMCU-falsher (only for Windows)](https://github.com/nodemcu/nodemcu-flasher)
 
## Backend
Will host the UI, a REST api to manage users, boards and their configuration. Also interact with board anytime the user request it or following some simple business logic/schedule..

__Technologies__
* Java 8 
* Spring/Spring Boot
* Maven
* JPA/Hibernate
* Websockets: To live update the frontend
* MQTT: To interact with the boards
* PostgreSQL: Will store user and boards related info.
* MongoDB: Will store the datapoints so a chart can be displayed in the UI
 
## Frontend
Simple UI to display the status of the boards and its measures. User management. It also allows to interact with board.

__Technologies__
* React
* Redux
* ES6
* Highcharts
* Websockets
 
## Cloud services
* [Heroku](https://www.heroku.com/): As the AS.
* [CloudMQTT](https://www.cloudmqtt.com/): As the broker for the communications between the backend and the boards.
* [PostgreSQL](https://www.elephantsql.com/): To store the users and board configuration.
* [mLab](https://mlab.com/): To store the details such as the temperature.
 
