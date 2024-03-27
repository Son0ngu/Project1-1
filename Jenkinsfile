node {
    stage('SCM') {
        git branch: 'main', credentialsId: '20225586', url: 'https://github.com/Son0ngu/Project1-1.git'
    }
    stage('SonarQube Analysis') {
        def scannerHome = tool 'SonarQube Scanner'
        withSonarQubeEnv() {
            sh "${scannerHome}/bin/sonar-scanner -Dsonar.java.binaries=. -Dsonar.projectKey=Project1 -Dsonar.login=sqa_1594a9d468361dd853d87bb98bde478a8b9a9130"
        }
    }
}

