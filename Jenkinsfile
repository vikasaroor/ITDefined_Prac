pipeline{

agent any 

stages{
    stage('First Checkout'){
        steps{
          checkout scmGit(branches: [[name: '*/main'], [name: '*/feature1']],
            extensions: [], 
            userRemoteConfigs: [[url: 'https://github.com/vikasaroor/ITDefined_Prac.git']])
            sh 'git branch -a'
        }
    } 
    stage('Second Stgae'){
        steps{
            echo 'Hello In Second' 

        }
    } 


}
}