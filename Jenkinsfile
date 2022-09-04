node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'maven';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=ahmedramzygi_sonar-java-web-app_AYMIZLw3bNVeIO-b4L6v"
    }
  }
}
