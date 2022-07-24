pipeline {
    agent {
        label '!windows'
    }

    environment {
        DISABLE_AUTH = 'true'
        DB_ENGINE    = 'sqlite'
    }

    stages {

        stage('Build') {
            steps {
                echo "Database engine is ${DB_ENGINE}"
                echo "DISABLE_AUTH is ${DISABLE_AUTH}"
                sh 'printenv'
                sh 'ls -ltr'
                sh 'cat my.properties'
            }
        }

        stage('Deploy') {
            steps {
//                 def props = readProperties  file: './my.properties'
//                 for (def key in props.keySet())
//                 {
//                     println "key = ${key}, value = ${props[key]}"
//                 }
                echo "Database engine is ${DB_ENGINE}"
                echo "DISABLE_AUTH is ${DISABLE_AUTH}"
                sh 'printenv'
            }
        }
    }
}