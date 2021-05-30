pipeline {
  agent  any 
  
  stages {
    stage("Biuld"){
      steps {
        parallel(
         "step 1": { echo "build started " }
        
        )
        
      }     
    }
    stage("Deploy"){
      steps {
        parallel(
          "step 1": { echo "build ended"  }
          "step 2": { echo "build ended"  }
            
        )
        
      }
     
    }
  
  }


}
