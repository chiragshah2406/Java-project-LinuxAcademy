pipeline
{
agent
    { 
     label 'master'
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
         archiveArtifacts artifacts:'dist/*.jar','buildnumber',fingerprint:true
}
}	    
}
	     




