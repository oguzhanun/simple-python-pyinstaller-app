pipeline{
    agent none
    stages{
        stage("build"){
            agent{
                docker{
                    image 'python:2-alpine'
                }
            }
            steps{
                sh 'python -m py_compile sources/add2vals.py soruces/calc.py'
                stash(name: 'compiled-results', includes: 'sources/*.py*')
            }
        }
    }
}
