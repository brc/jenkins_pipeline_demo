/* vim: set ft=groovy : */

pipeline {
    agent any
    stages {
        stage('Build') {
            agent {
                docker 'maven'
            }
            steps {
                /* https://issues.jenkins-ci.org/browse/JENKINS-33510 */
                sh 'cd demo && mvn -B clean validate compile package'
            }
        }
    }
}
