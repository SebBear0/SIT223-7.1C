pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo '--- Build Stage ---'
                echo 'This stage is responsible for compiling the program into something that can be executed.'
                echo 'Tool: Gradle'
                echo "Justification: Gradle can let you build your Java program using code, which is powerful in complicated build processes and also let's you use a familiar code editor rather then learn a new application UI."
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo '--- Unit and Integration Tests Stage ---'
                echo 'This stage is responsible for testing distinct segments of your code to ensure critical logic has not been broken by new changes.'
                echo 'Tool: JUnit'
                echo "Justification: JUnit is a very common tool for running unit and integrations tests. It can be used to run an entire suite of tests, and is the default for Gradle."
            }
        }

        stage('Code Analysis') {
            steps {
                echo '--- Code Analysis Stage ---'
                echo 'This stage is responsible for ensuring the code meets specific standards and has minimal code smells and formatting inconsistency.'
                echo 'Tool: SonarQube'
                echo "Justification: SonarQube can be used to deny code that doesn't pass a certain quality threshold (these are called Quality Gates). With this set up, low quality code will be blocked from merging automatically."
            }
        }

        stage('Security Scan') {
            steps {
                echo '--- Security Scan Stage ---'
                echo 'This stage is responsible for detecting vulnerabilities that are present in the code.'
                echo 'Tool: Snyk'
                echo "Justification: Snyk is a highly praised tool that can scan your project dependencies to determine if you are relying on vulnerable code and provides fixes for you. They also provide functionality to statically analyse your code with AI."
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo '--- Deploy to Staging Stage ---'
                echo 'This stage is responsible for deploying your program to a private environment that mimics a public release environment.'
                echo 'Tool: Terraform'
                echo "Justification: Terraform is an Infrastructure-as-Code tool, meaning you can write code to deploy it. Much more deterministic then someone clicking buttons in AWS, and you can keep this same code for deploying to production which help with consistency."
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo '--- Integration Tests on Staging Stage ---'
                echo "This stage is responsible for running tests on the staging environment to ensure functionality won't be broken in the production environment."
                echo 'Tool: Postman & Newman'
                echo "Justification: Postman is used to visually build relatively complex API requests in an application. To integrate this into the pipeline, Newman can be used to run requests made in Postman."
            }
        }

        stage('Deploy to Production') {
            steps {
                echo '--- Deploy to Production Stage ---'
                echo 'This stage is responsible for deploying to production, making it available to customers.'
                echo 'Tool: Ansible'
                echo "Justification: Ansible lets you deploy to a production environment with more reliability then something like a shell script, since it uses a declarative configuration. It also helps you avoid any downtime through a rolling release, where only 1 server is taken offline, updated, and turned back online at a time."
            }
        }
    }
}
