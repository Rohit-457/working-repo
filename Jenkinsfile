pipeline {
        agent any
        triggers {
                 pollSCM '* * * * * '
                }
        parameters {
                 choice choices: ['QA', 'UAT'], description: 'choose the server', name: 'ENVIRONMENT'
                }
        stages {
                stage (checkout){
                        steps{git 'https://github.com/Rohit-457/working-repo.git'}
                }
                stage (build){
                        steps{sh 'mvn install'}
                }
                stage (Deploy){
                        steps{sh cp /target/working.war /home/rohit/Documents/devops/apache-tomcat-9.0.93/webapps
                        }
                }
        }
}

