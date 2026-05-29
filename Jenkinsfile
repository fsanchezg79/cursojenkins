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
                        echo '[P1]Procesando datos1.txt'
                        echo "[P1]" 
                        sh 'cat datos1.txt'
                        sleep(5)
                    } 
                }
                stage('Procesar datos2.txt ') { 
                    steps { 
                        echo '[P2]Procesando datos2.txt'
                        echo "[P3] "
                        sh 'cat datos2.txt'
                        sleep(10)
                    } 
                }
                stage('Procesar datos3.txt ') { 
                    steps { 
                        echo '[P3]Procesando datos3.txt'
                        echo "[P3] "
                        sh 'cat datos3.txt'
                        sleep(15)
                    } 
                }
                stage('Proceso fallido') { 
                    steps { 
                        echo '[P4]Procesando fallar'
                        sh 'cat noexiste.txt'
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
