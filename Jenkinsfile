node {
stage("Git Clone"){

git branch: 'main', url: 'https://github.com/chanakyad/Facility.git'
}
stage("Docker build"){
sh 'docker build -t facility .'
sh 'docker images'
stage("Deploy"){
sh 'docker rm -f facility||true'
sh ' docker run -d -p 9001:9001 --name facility facility'
}
}
}
