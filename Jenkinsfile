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
                        ansiColor('vga') {
                        echo "[31m[P1]Procesando datos1.txt\033[0m"
                        echo "[31m[P1]\033[0m" 
                        }
                        sh 'cat datos1.txt'
                        sleep(5)
                    } 
                }
                stage('Procesar datos2.txt ') { 
                    steps {
                        ansiColor('vga') {
                        echo "[32m[P1]Procesando datos2.txt\033[0m"
                        echo "[32m[P1]\033[0m"
                        }
                        sh 'cat datos2.txt'
                        sleep(10)
                    } 
                }
                stage('Procesar datos3.txt ') { 
                    steps {
                        ansiColor('vga') {
                        echo "[33m[P1]Procesando datos2.txt\033[0m"
                        echo "[33m[P1]\033[0m"
                        }
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
