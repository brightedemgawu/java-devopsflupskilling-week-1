pipeline{
    agent any
    
    stages{
        
        stage("Initializing"){
            steps{
                echo "Initialization"
                bat "dir /B"
            }
        }
        
//         stage("fecthing"){
//             steps{
//                 git branch: 'master', url: 'https://github.com/brightedemgawu/java-devopsflupskilling-week-1.git'
//                 bat "dir /B"
//             }
//         }
        stage("build"){
            steps{
                bat "mvnw clean package"
        
            }
        }
        
        stage("testing"){
            parallel{
                stage("Test 1"){
                    steps{
                        echo "test set A"
                    }
                }
            }
        }
        
        stage("capture"){
            steps{
                archiveArtifacts '**/target/*.war'
        
            }
        }
    }
    
    post{
        always{
            echo "In posting"
        }

    }
}
