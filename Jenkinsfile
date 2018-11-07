#!/usr/bin/env groovy

pipeline {

    parameters {

        string(name: 'input_name',
            defaultValue: '',
            description: 'Input')

    }


    agent { label "master" }
     
    stages {
        stage("initial run") {
            when {
                expression {
                    params.input_name == ''
                }
            }
            steps {
                echo 'INITIAL RUN COMPLETED. JOB PARAMETERIZED.'
            }
        } 

        stage('echo input')  {
            when {
                expression {
                    params.input_name != ''
                }
            }
            steps {
                echo "${input_name}"
            }
        }
		
     }
}