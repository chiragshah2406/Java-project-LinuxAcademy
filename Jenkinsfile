pipeline
{
agent
    { 
     label 'master'
    }
options
{ 
buildDiscarder(logRotator(numToKeepStr: '2', artifactNumToKeepStr: '1'))
}
 stages{
    stage('Unit Tests') {
    steps {
         sh 'ant -f test.xml -v'
         junit 'reports/result.xml'
        }
     }


 
 
        
       
 stage('BUILD')
         {  
          steps 
             {
               sh 'ant -f build.xml -v'
                }
	     }
	     }
       post
        {
         success
         { 
         archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
}
}	    
}
	     




