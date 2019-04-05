def pipelineConfig = [
    maven: [
        tool: 'M3',
        settings_config: 'nexus_maven_settings'
    ]
]

JSLInit(pipelineConfig)

node {
    stage('test') {
        maven.compile('-DskipTests -Dmaven.test.failure.ignore')
    }
}
