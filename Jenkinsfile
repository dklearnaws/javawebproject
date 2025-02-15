pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                sh "mvn clean package"
            }
        }
        
         stage('Deploy'){
            steps{
                deploy adapters: [tomcat9(credentialsId: '119102c3-9697-4657-a66d-fd13337e0a43', path: '', url: 'ec2-3-135-191-53.us-east-2.compute.amazonaws.com')], contextPath: 'webapp2', war: '**/java-web-project.war'
            }
        }
    }
}
