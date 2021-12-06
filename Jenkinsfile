pipeline {
    agent any
    options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                def selection = input id: 'myChoice', message: 'please choose', parameters: [choice(name: 'test', choices: 'one\ntwo\nthree', description: 'which one')]
                echo "Testing ${selection}"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
}