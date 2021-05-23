node {
    Stage("one"){
        // building
        echo "I am Raj and he is running build ${env.BUILD_ID} on ${env.JENKINS_URL}"
        sh 'cp ./index.html /tar/'
    }
    Stage("two"){
        // converting
        
        sh "cd /tar"
        sh "tar -xvf ./"
    }
    Stage("three"){
        //uploading
         s3Upload(bucket:"appStore", workingDir:'prod', includePathPattern:'**/*');
    }
}
