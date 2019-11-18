# weather-services

**Prerequisite :- JDK 8**

## Executing the Weather SOAP Services

- The Weather Service is instantiated by executing the [Dockerfile](https://github.com/firzhan/weather-services/blob/master/weatherExcerciseDockerFile/Dockerfile).  
- First, we have to build the dockerfile provided for the backend services using the following command.  
   ```docker build -t deloitt/weather```
- Next we have to run the docker container on port 8080 using following command. 
   ```docker run -p 8080:8080 deloitt/weather:latest```


## Building the deployable JAR

- First, we have to navigate into the [WeatherServices folder](https://github.com/firzhan/weather-services/tree/master/weather-services) which contains the mule source. Execute the command ```mvn clean install``` at the parent POM to generate the JAR file.
- JAR file under the name weather-services-1.0.0-mule-application.jar could be found under the target folder of the Weather Services source directory.

## Executing the Mule EE Environment

- The latest version of Mule EE 4.2.1 could be downloaded over the following [link](https://www.mulesoft.com/lp/dl/mule-esb-enterprise) 
- Unzip the archive and copy the JAR file into the apps folder inside the root directory of the Mule EE distribution.

## API Invocation

- All the cities within the country coudl be easily accessible via following API
  ** http://localhost:8081/api/weather/v1/cities/Australia **

- API for fetching the status of weather in a city of a country
  ** http://localhost:8081/api/weather/v1/city?city=Perth&country=Australia **
