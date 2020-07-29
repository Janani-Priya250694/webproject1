pipeline{
agent any
  stages{
    stage('Compile') {
    steps{
      echo "Hello World"
         }
        }
       } 
post {
success { echo 'I will run for success'}
}
      
post {
failure { echo 'I will run for failure'}
}
}
