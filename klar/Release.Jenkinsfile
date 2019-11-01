// klar

String image    = env.JOB_NAME.split('/')[1]
String registry = "harik8/$image"
String tag      = env.VERSION

pipeline {
    agent {
    kubernetes {
      	cloud 'kubernetes'
      	label 'klar'
      	defaultContainer 'jnlp'
      	yamlFile "$image/pod.yaml"
      }
    }
    
    environment {
        DOCKER_CREDENTIALS=credentials("DOCKER_CREDENTIALS")
    }

    stages {
        stage("release") {
            steps {
                container(name: 'kaniko', shell: '/busybox/sh') {
                     withEnv(['PATH+EXTRA=/busybox:/kaniko']) {
                      sh """#!/busybox/sh
                        /kaniko/executor --context=$WORKSPACE/$image --destination $registry:$tag
                      """
                     }
                }
            }
        }
    }
}
