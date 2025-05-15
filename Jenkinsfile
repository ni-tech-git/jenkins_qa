// global variables
// used across steps and stages
// persistent 
// Used in the groovy script

pipeline{
    agent any

    environment {
        // USed for shell variables. Passinmg to sh. exists whilst pipeline runs
        //creds/paths + in builts

    }

    options{
        timestamps()
        disableconcurrentbuilds()
        timeout(time: 10, unit "minutes")
        retry(5) stage

    }
}

stages{
    stage("Make a directory"){
        options{timeout(time: 1, unit: 'MINUTES')}
        steps{
            sh "mkdir ~/jenkins-dir"
            }
        post{
            success{
                echo "this was successful"
            }
            failure{
                echo "failed"
            }
            always{
                echo "this always prints"
            }
        }
    }
    stage("add file"){
        steps{
            sh "touch ~/jenkins-dir/file.txt"
        }
    }





}