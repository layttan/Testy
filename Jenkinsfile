node {
    git url: 'https://github.com/layttan/Testy.git'

    // Get Artifactory server instance, defined in the Artifactory Plugin administration page.
    def server = Artifactory.server "SERVER_ID"

    stage "Create build output"

        // Make the output directory.
        sh "mkdir -p output"

        // Write an useful file, which is needed to be archived.
        writeFile file: "output/usefulfile.txt", text: "This file is useful, need to archive it."

        // Write an useless file, which is not needed to be archived.
        writeFile file: "output/uselessfile.md", text: "This file is useless, no need to archive it."

    stage "Archive build output"

        // Archive the build output artifacts.
        archiveArtifacts artifacts: 'output/*.txt', excludes: 'output/*.md'


}