node{

def mavenHome = tool name: "Maven3.6.3"

stage('CheckoutCode'){
 git branch: 'development', credentialsId: '7c8519fc-76d6-48fd-9726-245714d9ccd9', url: 
'https://github.com/vijaysoftwaresolutions-ec-projects/maven-web-application.git'
}

stage ('Build'){
sh "${mavenHome}/bin/mvn clean package"
}

/*
stage ('ExecuteSonarQubeReport'){
sh "${mavenHome}/bin/mvn sonar:sonar"
}

stage ('UploadArtifacteIntoNexus'){
sh "${mavenHome}/bin/mvn deploy"
}

stage('DeployAppIntoTomcatServer')
{
sshagent(['c366e2d2-f491-4ef2-9a39-9904e5cecf36']) {
 sh "scp -o StrictHostKeyChecking=no taregt/maven-web-application.war 
ec2-user@65.1.134.143:/opt/apache-tomcat-9.0.50/webapps"   
}
}

stage('SendEmailNotification')
{
emailext body: '''Build Over!...

Regards,
Vijayakumar Degala,
8970000161''', subject: 'Build Over!!', to: 'vijaydevops9396@gmail.com,krishnady.naidu@gmail.com'
}
*/

}
