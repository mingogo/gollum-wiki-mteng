1. Download the SonarQube on the official site
2. Download the libraries from d01 and copy those into {$sonarHome}/extensions/plugins
3. Export the Sonar Quality Profiles from f10
4. Once start the sonar server, import the sonar profiles
5. In the master pom file, add one line: <sonar.sources>src/main</sonar.sources>
6. Once everything is in place, build the project using sonar goal: mvn sonar:sonar
