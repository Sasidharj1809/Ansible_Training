#!/usr/bin/env groovy

node('Agent') {
    timestamps {
        deleteDir()

        // Checkout the app at the given commit sha from the webhook
        checkout scm
        def WORKSPACE = pwd()
        "echo '$WORKSPACE'"

        //ansiblePlaybook{
        //         playbook: '$WORKSPACE/playbook-multiplecommands.yaml'
        //         inventory: '$WORKPSACE/inventory.txt'
         //        colorizedOutput: true}
        sh "echo '$PWD'"
        sh "ansible-playbook playbook-multiplecommands.yaml -i inventory.txt"
        sh "echo 'WE ARE DEPLOYING'"
        }
    }