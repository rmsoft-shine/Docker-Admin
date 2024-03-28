node {
     stage('Clone repository') {
         checkout scm
     }

     stage('Build image') {
         app = docker.build("my-first-pipeline") //이미지 이름 설정
     }
     stage('Push image') {
                script {
                    sh 'docker run -d -p 18000:18000 my-first-pipeline'
                }
     }
 }

 //도커 run -> build 된 파일 실행