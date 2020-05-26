node {
  stage 'Checkout'
  git 'ssh://git@github.com:aneestalha/DevopsDemo.git'
 
  stage 'Docker build'
  docker.build('demo')
 
  stage 'Docker push'
  docker.withRegistry('https://340269247939.dkr.ecr.us-east-2.amazonaws.com', 'ecr:us-east-2:demo-ecr-credentials') {
    docker.image('demo').push('latest')
  }
}
