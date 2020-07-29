pipeline{
agent any
trigeers {
pollSCM("* * * * *")
}
  stages{
    stage('Compile') {
    steps{
      echo "Hello World"
         }
        }
       } 
post {
failure { 
echo 'I will run for failure'
}
}
 }   
