@Library('piper-lib-os') _
node() {
    env.NODEJS_HOME = "${tool 'node'}"
    env.PATH="${env.PATH}:$(env.NODEJS_HOME}/bin"
    sh 'npm --version'
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }    
    stage('build') {
        mtaBuild script: this
    }    
}
