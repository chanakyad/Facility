node {
stage("Git Clone"){

git branch: 'master', url: 'https://github.com/chanakyad/eurekaserver1.git'
}
stage("Docker build"){
sh 'docker build -t customer .'
sh 'docker images'
stage("Deploy"){
sh 'docker rm -f customer||true'
sh ' docker run -d -p 9001:9001 --name customer customer'
}
}
}
