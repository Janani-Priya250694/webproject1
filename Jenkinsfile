pipeline{
agent any
triggers {
pollSCM("* * * * *")
upstream(upstreamProjects: 'triggers', threshold: hudson.model.Result.SUCCESS) }
environment{
   JENKINS_CRD = credentials('slack_crd1')
}
  stages{
    stage('Compile') {
    steps{
      echo "Hello World"
      sh 'echo SLACKUSER : $JENKINS_CRD' 
         }
        }
       } 
post {
success {
echo 'I will run for success and will send notification to slack'
slackSend channel: '#devops-concepts', message: env.BUILD_ID + 'completed'
}

failure { 
echo 'I will run for failure'
}
}
 }   
