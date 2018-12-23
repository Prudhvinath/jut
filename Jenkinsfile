// Declarative //
pipeline {
agent any
stages {
            stage('SBuild') {
                steps {
                echo 'Building..'
                }
            }
            stage('STest') {
                steps {
                echo 'Testing..'
                }
            }
            stage('SDeploy') {
                steps {
                echo 'Deploying....'
                }
            }
            
           
          stage('Build') {
                steps {
                  
                  archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true 
				  echo 'success'
                  }
                }
          stage('Test') {
                steps {
                /* `make check` returns non-zero on test failures,
                * using `true` to allow the Pipeline to continue nonetheless
                */
                 
                junit '**/target/surefire-reports/*.xml' 
                }
            }
            
    }
}
