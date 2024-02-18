pipeline{
     agent any
        stages {
           stage('Build Application') {
              steps {
                   bat 'mvn clean install'
                    }
                 }
          stage('Deploy CloudHubs') {
              environment {
         ANYPOINT_CREDENTIALS = credentials('62da5af8cdfd46978e9e9efb43912add')
               }
              steps {
                    echo 'Deploying mule project due to the latest code commit…'
                    echo 'Deploying to the configured environment….'
                    bat 'mvn clean deploy -DmuleDeploy -Dmule.app.name=CICD -Dusername=habtamu123-Dpassword=HABcdiHOPE@2024 -DworkerType=Micro -Denv='dev'
                            }
                       }
                }
        }