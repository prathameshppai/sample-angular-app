node {
    stage('Checkout') {
      cleanWs()
      git url: 'https://github.com/prathameshppai/sample-angular-app.git'
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
