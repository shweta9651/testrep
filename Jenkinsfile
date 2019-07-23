@Library('piper-lib-os') _
node() {
    tool name: 'node', type: 'nodejs'
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }    
    stage('build') {
        mtaBuild script: this
    }    
}
