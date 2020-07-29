pipeline{
agent any
triggers {
cron("* * * * *")
upstream(upstream(upstreamProjects: 'triggers', threshold: hudson.model.Result.SUCCESS) }
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
