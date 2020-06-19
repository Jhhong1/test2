@Library('alauda-cicd') _
def APP
pipeline {
    agent any
    parameters {
        string(name: 'COMPONENT', defaultValue: '', description: 'The component of the chart worked on. Will be used to update the values.yaml file.')
    }
    stages {
        stage('Clone') {
            steps {
                script {
                    def causes = currentBuild.getBuildCauses()
                    def specificCause = currentBuild.getBuildCauses('hudson.model.Cause$UserIdCause')
                    echo "specificCause: ${specificCause}"
                    echo "current branch: ${BRANCH}"
                }
            }
        }
    }
}
