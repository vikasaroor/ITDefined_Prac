pipeline{

agent any

options {
  buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '5')
}

stages{
    stage('First Checkout'){
        agent {
             label 'testSlave || sseNode' 
        }       
        steps{
          checkout scmGit(branches: [[name: '*/feature1']],
            extensions: [], 
            userRemoteConfigs: [[url: 'https://github.com/vikasaroor/ITDefined_Prac.git']])
            sh 'git branch -a'
            sh 'git branch '
            sh 'hostname -i'

        }
    } 
    stage('Second Stgae'){
        steps{
            echo 'Hello In Second' 
            sh 'hostname -i'

        }
    } 

}
}