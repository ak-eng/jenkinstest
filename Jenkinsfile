node("vm-15") {

    stage("Checkout") {
        checkout scm
    }


    stage "Build"
    /* Build the Docker image with a Dockerfile, tagging it with the build number */
    def app = docker.build "genia_one_build"

    stage "RunTheBuildCommand"
    /* We can run tests inside our new image */
    app.inside {
                sh 'cat README;cat /etc/lsb-release'
    }



}
