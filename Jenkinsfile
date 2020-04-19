pipeline {
 agent any
 tools {
  maven 'M3'
 }
 stages {
  stage('Build') {
   steps { 
    sh 'mvn clean test'
    }
  }    
  
  
stage('reports') {
   	steps {
  	script {
  			allure ([
  			        includePropertoes: false,
  			        jdk: '',
  			        properties:[],
  			        reportBuildPolicy: 'ALWAYS' ,
  			        results: [[path: '/allure-results']]  
  			])	        
   			
   			// publish html
   			publishHTML([
   			allowMissing: false,
   			alwaysLinkToLastBuild: false,
   			keelAll: false,
   			reportDir: 'build',
   			reportFiles: 'Test_xecutionReport.html',
   			reportName: 'Extent HTML Report',
   			reportTitles: ''
   			])
   	
   	}
   	}
}  			
   			
}  			
   			
} 			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			
   			