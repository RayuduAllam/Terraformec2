pipeline {

    agent {

        node {

            label 'master'
        }

    }

    stages {

        stage('terraform started') {

            steps {

                sh 'echo "Started...!" '

            }

        }

        stage('git clone') {

            steps {

                sh 'sudo rm -r *;sudo https://github.com/RayuduAllam/Terraformec2.git'

            }

        }

        stage('tfsvars create'){

            steps {

                sh 'sudo cp /home/ubuntu/vars.tf ./jenkins/'

            }

        }

        stage('terraform init') {

            steps {

                sh 'sudo /home/ubuntu/terraform init ./jenkins'

            }

        }

        stage('terraform plan') {

            steps {

                sh 'ls ./jenkins; sudo /home/ubuntu/terraform plan ./jenkins'

            }

        }

        stage('terraform ended') {

            steps {

                sh 'echo "Ended....!!"'

            }

        }



        

    }

}
