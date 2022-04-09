node {
    stage('Checkout') {
      cleanWs()
      git credentialsId: '7cbce867-da7d-4aa9-9bfc-3c5fa97cada3', url: 'https://github.com/prathameshppai/sample-angular-app.git'
    }

    stage('Build') {
      nodejs('node') {
          sh 'npm install'
          sh 'ng lint'
          sh 'npm run test --watch=false'
          sh 'ng build --configuration production'
        }
    }
}
