pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
             	step{ git 'https://github.com/georgianaanton/learnJenkins'}
             	step{ tool name: 'Maven', type: 'maven'
             			sh 'mvn clean compile package'
             	}
              
            }
        }
        stage('Example Deploy') {
            when {
                branch 'production'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}