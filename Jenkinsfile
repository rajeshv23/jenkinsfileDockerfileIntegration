node {
    checkout scm

    withEnv(['HTTPS_PROXY=http://forwardproxy:3128']) {
        docker.withServer('tcp://10.39.152.14:2375', 'swarm-certs') {
        docker.image('mysql:5').withRun('-p 3306:3306') {
            /* do things */
        }
        }
    }
    
}
