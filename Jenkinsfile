// pipeline {
//     agent any

//     stages {
//         stage('Clone Git') {
//             steps {
//                 git 'https://github.com/cthien24032002/learn-cicd-jetkin.git'
//             }
//         }

//         stage('Build Docker Image') {
//             steps {
//                 script {
//                     docker.build('jenkins-demo-image')
//                 }
//             }
//         }

//         stage('Run Docker Container') {
//             steps {
//                 script {
//                     sh 'docker run -d -p 3000:3000 --name jenkins-demo-container jenkins-demo-image'
//                 }
//             }
//         }

//         // Optional: Push to Docker Hub
//         stage('Push Docker Image') {
//             steps {
//                 withCredentials([usernamePassword(credentialsId: 'docker-hub-credentials', usernameVariable: 'DOCKER_USER', passwordVariable: 'DOCKER_PASS')]) {
//                     script {
//                         sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'
//                         sh 'docker tag jenkins-demo-image $DOCKER_USER/jenkins-demo-image'
//                         sh 'docker push $DOCKER_USER/jenkins-demo-image'
//                     }
//                 }
//             }
//         }

//         stage('Cleanup') {
//             steps {
//                 script {
//                     sh 'docker rm -f jenkins-demo-container || true'
//                 }
//             }
//         }
//     }
// }
pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-image .'
            }
        }
    }
}
