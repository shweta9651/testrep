@Library('piper-lib-os') _
node() {
    agent any
    tools {nodejs "node"}
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }    
    stage('build') {
        mtaBuild script: this
    }    
}
