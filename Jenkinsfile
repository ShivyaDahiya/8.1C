pipeline {
  agent any

  environment {
    REPO = "https://github.com/ShivyaDahiya/8.1C.git"
    JOB_EMAIL = "shivyadahiya2002@gmail.com"
  }

  stages {
    stage('Build') {
      steps {
        echo 'Compile and package the application code into deployable artifacts'
        echo 'Maven'
      }
    }

    stage('Unit and Integration Tests') {
      steps {
        echo 'Run unit tests to verify individual modules work correctly and integration tests to ensure components interact as expected'
        echo 'JUnit'
      }
    }

    stage('Code Analysis') {
      steps {
        echo 'Perform static code analysis to identify code smells, enforce coding standards, and ensure code quality'
        echo 'Checkstyle'
      }
    }

    stage('Security Scan') {
      steps {
        echo 'Scan code and dependencies for vulnerabilities and known security issues'
        echo 'Snyk, OWASP Dependency-Check'
      }
    }

    stage('Deploy to staging') {
      steps {
        echo 'Simulating manual approval: pipeline will pause for 10 seconds'
      }
    }

    stage('Integration Tests on Staging') {
      steps {
        echo 'Run tests in the staging environment to ensure application behaves as expected in a production-like setup'
        echo 'Postman/Newman (API tests), Selenium (UI tests), JUnit/TestNG for integration tests'
      }
    }

    stage('Deploy to production') {
      steps {
        echo 'Deploy the application to production servers after successful testing and validation'
        echo 'AWS EC2 / AWS CodeDeploy, Terraform'
      }
    }
  }

  post {
    success {
      echo 'Pipeline completed successfully'
    }
    failure {
      echo 'Pipeline failed'
    }
  }
}
