pipeline {
  agent  any 
  
  stages {
    stage("Biuld"){
      steps {
        echo "build started "
         script {
          withCredentials([
            usernamePassword(credentialsId: 'myacr',
              usernameVariable: 'username',
              passwordVariable: 'password')
          ]) {
            print 'username=' + username + 'password=' + password

            print 'username.collect { it }=' + username.collect { it }
            print 'password.collect { it }=' + password.collect { it }
          }
       
        
      }     
    }
    stage("Deploy"){
      steps {
        parallel(
          "step 1": { echo "build ended"  },
          "step 2": { echo "build ended"  }
            
        )
      }
    }
  }
}
