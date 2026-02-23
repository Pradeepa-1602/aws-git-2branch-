pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                sh 'https://github.com/Pradeepa-1602/aws-git-2branch-/new/main'
                sh 'cd your-repo'
            }
        }

        stage('Commit & Push') {
            steps {
                dir('your-repo') {
                    sh '''
                        git config user.name "jenkins"
                        git config user.email "jenkins@gmail.com"

                        echo "Updated by Jenkins" >> test.txt

                        git add .
                        git commit -m "Auto commit"
                        git push origin main
                    '''
                }
            }
        }
    }
}
