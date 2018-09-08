#!/usr/bin/env groovy

node('master') {
    timestamps {
        deleteDir()

        // Checkout the app at the given commit sha from the webhook
        checkout scm
        def WORKSPACE = pwd()
        ansiblePlaybook{
                 playbook: "$WORKSPACE/playbook-multiplecommands.yaml",
                 inventory: "$WORKPSACE/inventory.txt",
                 colorizedOutput:true
        }
    }
}