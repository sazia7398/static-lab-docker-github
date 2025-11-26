pipeline {
agent any

stages {

stage('Checkout from GitHub') {
steps {
git branch: 'main', url: 'https://github.com/sazia7398/static-lab-docker-github.git'
}
}

stage('Build Docker Image') {
steps {
bat 'docker build -t static-site:85 .'
}
}

stage('Run Container') {
steps {
bat 'docker run -d -p 5080:80 --name sazia static-site:85'
}
}
}
}
