pipeline{

agent {
    label 'testSlave && sseNode' 
}

stages{
    stage('First Checkout'){
        steps{
          checkout scmGit(branches: [[name: '*/feature1']],
            extensions: [], 
            userRemoteConfigs: [[url: 'https://github.com/vikasaroor/ITDefined_Prac.git']])
            sh 'git branch -a'
            sh 'git branch '
        }
    } 
    stage('Second Stgae'){
        steps{
            echo 'Hello In Second' 

        }
    } 

}
}