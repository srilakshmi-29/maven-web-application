node {
    def mavenHome = tool name:"Maven 3.9.4"

stage('checkoutcode'){

    git branch: 'development', credentialsId: '7fbffbb9-cbcd-4a18-9d9e-8c1b262cde83', url: 'https://github.com/srilakshmi-29/maven-web-application.git'
}

stage('build'){

    sh "${mavenHome}/bin/mvn clean package"
}
/*
stage('Execute SonarQube Report'){
    sh "${mavenHome}/bin/mvn clean sonar:sonar"
}

stage('creating Artifactory'){
    sh "${mavenHome}/bin/mvn clean deploy"
}

stage('DeployAppIntoTomaCat'){
    sshagent(['f3a0b0df-8fc4-4617-879f-83bcc9246b2e']) {
    sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/icicibank-pipeline/target/maven-web-application.war ec2-user@16.171.19.229:/opt/apache-tomcat-9.0.80/webapps"
}
}
*/
}
