@Library('SharedLibrary1@main')_
node('general'){
    tools {
        maven 'maven3.6.3'
    }
    ansiColor('xterm'){
        env.LOG_LEVEL = "INFO"
        println "System log level is set  to: " + env.LOG_LEVEL
        
        env.AppLogLevel = "ALL" 
        println "Application log level is set to: " + env.AppLogLevel
        
        withEnv(['APP_LOG_LEVEL=' + env.AppLogLevel ]) {
            jenkinsfile()
        }
    }
}
