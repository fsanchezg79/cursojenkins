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
                        echo "\e[31m[P1]Procesando datos1.txt\e[0m\n"
                        echo "\e[31m[P1]\e[0m\n" 
                        sh 'cat datos1.txt'
                        sleep(5)
                    } 
                }
                stage('Procesar datos2.txt ') { 
                    steps { 
                        echo "\033[31m[P2]Procesando datos2.txt\033[0m\n"
                        echo "\033[31m[P3]\033[0m\n "
                        sh 'cat datos2.txt'
                        sleep(10)
                    } 
                }
                stage('Procesar datos3.txt ') { 
                    steps { 
                        echo "\x1b[31m[P3]Procesando datos3.txt\x1b[0m\n"
                        echo "\x1b[31m[P3]\x1b[0m\n "
                        sh 'cat datos3.txt'
                        sleep(15)
                    } 
                }
            } 
        }
        stage('Resumen') {
             steps { 
                 echo "Todos los porcesos han finalizado correctamente"
             }
        }
    }
}
