properties(
        [
                buildDiscarder(
                        logRotator(artifactDaysToKeepStr: '',
                                artifactNumToKeepStr: '',
                                daysToKeepStr: '10',
                                numToKeepStr: '10'
                        )
                ),
                durabilityHint('MAX_SURVIVABILITY'),
                disableConcurrentBuilds(),
                disableResume(),
                [
                        $class      : 'CopyArtifactPermissionProperty',
                        projectNames: '*'
                ],
                parameters(
                        [
                                booleanParam(
                                        defaultValue: true,
                                        description: 'Do you want to use mounted maven?',
                                        name: 'MOUNT_MAVEN'
                                ),
                                string(
                                        defaultValue: 'N/A',
                                        description: 'To build a branch',
                                        name: 'BUILD_BRANCH',
                                        trim: true
                                ),
                                string(
                                        defaultValue: 'N/A',
                                        description: 'To build a tag',
                                        name: 'USER_BUILD_TAG',
                                        trim: true
                                )
                        ]
                )
        ])

pipeline {
    agent any
    stages {
        stage('build the code') {
            steps {
                echo "code build successfully"
            }
        }
    }
}