pipeline {
     // Ejecutamos en el nodo principal
     agent {
         node {
             label 'master'
         }
     }
          
     // Asignamos variables de entorno
     environment {
        NOMBRE_TEST="saludooooooozzzz"
     }
     
     stages {
         stage('Configuracion base') {
             steps {
                echo "${NOMBRE_TEST}"
	         }
         }

         stage('Build QA') {
             steps {
                 sh 'whoami'
                 sh 'whoami'
	         }
         }
         
         stage('Deploy SSH QA') {
             steps {          
                sh 'whoami'
                sh 'whoami'           
            }
         }

         stage('Aprobacion despliegue produccion') {
             input {
                 message "Esta seguro que desea desplegar a producción?"
                 ok "Aprobar"
                 parameters {
                     string(name: 'comentario', defaultValue: ' ', description: 'Deje aquí su comentario')
                 }
             }
             steps {
                 echo "${comentario}"
             }
         }

         stage('Build PROD') {
             steps {
                 sh 'whoami'
                 sh 'whoami'
	         }
         }

         stage('Deploy SSH PROD') {
             steps {
                 sh 'whoami'
                 sh 'whoami'
             }
         }
        
     }       
}