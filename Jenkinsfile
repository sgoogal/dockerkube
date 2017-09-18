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

stage('build and publish to Nexus') {
        sh 'gradle clean install uploadArchives'
    }
}
