def gitCommit() {
    sh "git rev-parse HEAD > GIT_COMMIT"
def gitCommit = readFile('GIT_COMMIT').trim()
    sh "rm -f GIT_COMMIT"
    return gitCommit
}

node {
    // Checkout source code from Git
    stage 'Checkout'
    //sh "python3 -m pip freeze"
    
    
    checkout scm

    // Build Docker image
   stage 'Train Model(s)'
   echo "$path" 
    
   echo 'Test accuracy and measure inference time.'
     

   sh 'python --version'
   sh 'python3 --version' 
   
   sh 'python3 wine_mlflow.py 0.999 0.999'
   
   sh 'sleep 10'

  stage 'Optimize Model(s)'
  echo 'Test accuracy and measure inference time.'
  sh 'sleep 5'

  // Test
  stage 'Test' 
  echo 'Test accuracy and measure inference time.'

  // Test
  stage 'Build Serving container'
  echo 'Build TensorFlow Serving Container.'

  
}
