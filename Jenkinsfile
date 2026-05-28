pipeline {
    agent any

    stages {
        stage('Deploy') {
            steps {
                writeFile file: 'saludo.txt', text: 'Hola Jenkins'
            }
        }
    }
}
