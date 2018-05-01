pipeline
{
agent
    { 
     label 'master'
    }
options
{ 
buildDiscarder(logRotator(numtoKeepStr: '2', artifactNumToKeepStr: '1'))
}
 stages
      { stage('BUILD')
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
	     




