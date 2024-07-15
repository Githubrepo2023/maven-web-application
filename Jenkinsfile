node
{
    def mavenHome = tool name: "maven"
    stage ('checkout code')
    {
        git credentialsId: '4d9e62e7-cb93-4450-b5c8-ea303fc7edb9', url: 'https://github.com/Githubrepo2023/maven-web-application.git'
    }
    
    stage ('build the code')
    {
        sh "${mavenHome}/bin/mvn clean package"
    }
    
    /*
    stage ('excute the sonarquebe server')
    {
        sh "${mavenHome}/bin/mvn clean sonar:sonar"
    }
     stage ('Deployee the application into tomcat server')
     {
         sshagent(['a05db061-67e4-4d8c-964c-9ce72072fe96']) {
    sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@172.31.8.210:/opt/apache-tomcat-9.0.91/webapps/"
}
     }
     */
}//node closing
