pipeline {
    agent any
    tools {
        maven 'maven'
    }

    stages {
         stage('Clean wrokspace') {
            steps {
                cleanWs()
            }
        }
        stage('Pull') {
            steps {
                git branch: 'main', url: 'https://github.com/rodeaayush/demo_repo.git'
                echo 'pull successfull'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
                echo 'Here we are deploying the code'
            }
        }
        //         stage('Test') {
        //     steps {
        //         sh '/opt/apache-maven-3.9.6/bin/mvn sonar:sonar -Dsonar.projectKey=studentapp-ui -Dsonar.host.url=http://54.221.44.130:9000 -Dsonar.login=f316d47655ec5d539cb484f38aa1f1666c491815'
        //         echo 'Testing done'
        //     }
        // }
        //         stage('Deploy') {
        //     steps {
        //         echo 'Deploy done'
        //     }
        // }
    }
}
