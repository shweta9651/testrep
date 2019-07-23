@Library('piper-lib-os') _
node() {
    sh 'npm --version'
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }    
    stage('build') {
        mtaBuild script: this
    }    
}
