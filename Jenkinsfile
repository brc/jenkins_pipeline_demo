/* vim: set ft=groovy : */

pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker 'maven'
            }
            steps {
                sh 'mvn -h'
                sh 'ls -l /.dockerenv || true'
                sh 'cat /proc/1/cgroup'
            }
        }
    }
}
