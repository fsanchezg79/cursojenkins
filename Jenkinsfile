pipeline {
    agent any

    stages {
        stage('Preparacion') {
            steps {
                echo 'Preparando el entorno...'
                sh 'ls'
            }
        }
        stage('Procesamiento en paralelo') {
           parallel {
                stage('Procesar datos1.txt ') { 
                    steps { 
                        echo 'Procesando datos1.txt'
                        sh 'cat datos1.txt'
                        sleep(5000)
                    } 
                }
                stage('Procesar datos2.txt ') { 
                    steps { 
                        echo 'Procesando datos2.txt'
                        sh 'cat datos2.txt'
                        sleep(10000)
                    } 
                }
                stage('Procesar datos3.txt ') { 
                    steps { 
                        echo 'Procesando datos3.txt'
                        sh 'cat datos3.txt'
                        sleep(15000)
                    } 
                }
            } 
        }
    }
}
