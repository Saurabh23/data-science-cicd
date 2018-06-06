def gitCommit() {
    sh "git rev-parse HEAD > GIT_COMMIT"
def gitCommit = readFile('GIT_COMMIT').trim()
    sh "rm -f GIT_COMMIT"
    return gitCommit
}

node {
    // Checkout source code from Git
    stage 'Checkout'
    checkout scm

    // Build Docker image
   stage 'Train Model(s)
   echo 'Test accuracy and measure inference time.'


  stage 'Optimize Model(s)'
  echo 'Test accuracy and measure inference time.'


  // Test
  stage 'Test' 
  echo 'Test accuracy and measure inference time.'

  // Deploy
 stage 'Deploy'

    marathon(
        url: 'http://marathon.mesos:8080',
        forceUpdate: false,
        filename: 'marathon.json',
    )
}
