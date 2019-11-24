pipeline {
 agent none
    stages {
      stage('SCM_Chekout') {
          agent { label 'master' }
	steps {
	  checkout([$class: 'GitSCM', 
                branches: [[name: '*/master']], 
                doGenerateSubmoduleConfigurations: false, 
                extensions: [], submoduleCfg: [], 
                userRemoteConfigs: [[url: 'https://github.com/KhanSahab/Maven-petclinic-project-1.git']]])
            }
        }

     stage('code-validation') {
         agent { label "master" }
	steps {
                       sh 'mvn -f pom.xml sonar:sonar'
            }
        }
     stage('Test and package') {
          agent { label "master" }
	steps {
                      sh 'mvn -f pom.xml package'
        }
      }
    }
  }
	                checkout([$class: 'GitSCM',
                	   branches: [[name: '*/master']],
                    	   doGenerateSubmoduleConfigurations: false,
                    	   extensions: [],
                     	   submoduleCfg: [],
                    	   userRemoteConfigs: [[url: 'https://github.com/deshshank/Maven-petclinic-project.git']]])
            }
        }
       
     //   stage('code-validation') {
     //   agent { label "master" }
//	steps {
     //                  bat 'mvn -f pom.xml sonar:sonar'
  //          }
   //     }
     stage('Test and package'){
          agent { label "master" }
	     steps {
                      bat 'mvn -f pom.xml package'
            }
        }
     
  }
}
>>>>>>> 291e13ef23b3303fc1faaeddd4e38db9d905a28d
