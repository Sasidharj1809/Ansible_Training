#!/usr/bin/env groovy

node('Agent') {
    timestamps {
        deleteDir()

        // Checkout the app at the given commit sha from the webhook
        checkout scm
        def WORKSPACE = pwd()
        "echo '$WORKSPACE'"

        //ansiblePlaybook{
        //         playbook: "$WORKSPACE/playbook-script-module.yaml"
        //         inventory: "$WORKPSACE/inventory.txt"
        //         colorized: true
        //         extras: "--syntax-check"
        //}

        sh "echo '$PWD'"
        sh "ansible-playbook playbook-script-module.yaml -i inventory.txt"
        sh "echo 'WE ARE DEPLOYING'"
        }
    }