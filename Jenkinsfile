node {

stage('checkout scm'){
checkout([$class: 'GitSCM',
branches: [[name: '*/master']],
doGenerateSubmoduleConfigurations: false,
extensions: [],
submoduleCfg: [],
userRemoteConfigs:
[[url: 'git@github.com:sgoogal/dockerkube.git']]])
        }

stage('switch user to root') {
        sh 'sudo su'
    }


stage('switch user to root') {
        sh 'cd $WORKSPACE'
    }

stage('build and publish to Nexus') {
        sh 'gradle upload'
    }
}
