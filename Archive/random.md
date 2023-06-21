## Maven + SonarQube 
mvn clean sonar:sonar \
  -Dsonar.projectKey=JavaWebApp \
  -Dsonar.host.url=http://44.203.4.255:9000 \
  -Dsonar.login=<sonarqube prject token>

## Before Running the `deploy` Command make sure to update the Nexus pom.xml and settings.xml with Nexus IP addedd, Username and Password. Make sure the plugings are defined as well
mvn clean package sonar:sonar \
  -Dsonar.projectKey=JavaWebApp-Project3 \
  -Dsonar.host.url=http://44.203.4.255:9000 \
  -Dsonar.login=<sonarqube prject token>

## Clean, Build, Test and Deploy(to Nexus)
mvn clean package sonar:sonar deploy \
  -Dsonar.projectKey=maven-java-webapp \
  -Dsonar.host.url=http://10.0.0.71:9000 \
 -Dsonar.login=678f20d3b9f0ee4d5d02cd6cc0cbd07b0dd1023c
