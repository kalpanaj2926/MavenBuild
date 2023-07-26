node(){

    stage('Code CheckoutKALPANA-1'){
        checkout scm
    }
    stage('Build'){
        sh "mvn clean install"
    }
    stage('archiveArtifacts'){
        
            archiveArtifacts artifacts: 'target/*.war'
        
        
    }
        stage('teststage'){
        
            echo 'testing' 
    
    }
    stage('teststage 4 CODE SCANNING DEMO FOR Kalpana'){
        
            echo 'kalpana code scanning' 
        
    }

    stage('Code Deployment'){
        
        deploy adapters: [tomcat9(credentialsId: 'tomcatcredentials', path: '', url: 'http://3.142.251.193:8080//')], contextPath: 'KALPANA_deploy', war: 'target/*.war'
    }
}
