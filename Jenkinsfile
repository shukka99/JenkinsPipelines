pipeline {
 agent any
 environment {
 DOCKER_USER = 'shukka'
 }
 stages {
 stage('Login Docker') {
 steps {
 withCredentials([string(credentialsId: 
'CHARLIE_DOCKER_PASSWORD', variable: 'DOCKER_PASS')]) {
 sh 'echo $DOCKER_PASS | docker login -u 
$DOCKER_USER --password-stdin'
 }
 }
 }
 }
}