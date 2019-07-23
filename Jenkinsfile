@Library('piper-lib-os') _
node() {
    env.NODEJS_HOME = "${tool 'Node 6.x'}"
    env.PATH="$(env.NODEJS_HOME}/bin:${env.PATH}"
    sh 'npm --version'
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }    
    stage('build') {
        mtaBuild script: this
    }    
}
