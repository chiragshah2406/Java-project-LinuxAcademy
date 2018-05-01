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
         archive 'dist/*.jar'
}
}	    
}
	     




