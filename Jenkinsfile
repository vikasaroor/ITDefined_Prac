pipeline{

agent any

options { 
    buildDiscarder logRotator(numToKeepStr: '5')
    timeout (time: 5, unit: 'HOURS')
}

parameters {
  booleanParam (defaultValue: false, description: 'Add to get', name: 'Test')
  choice (name: 'enviroment',choices:['prod','prepod','test'],description: 'Add ur Req value')
}


stages{
    stage('First Checkout'){
        
        steps{
          checkout scmGit(branches: [[name: '*/feature1']],
            extensions: [], 
            userRemoteConfigs: [[url: 'https://github.com/vikasaroor/ITDefined_Prac.git']])
            sh 'git branch -a'
            sh 'git branch '
            sh 'hostname -i'
            echo ${params.enviroment}
            echo ${params.name}
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