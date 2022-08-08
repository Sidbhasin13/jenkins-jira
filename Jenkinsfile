pipeline {
  agent any
  environment {
    BRANCH = "${BRANCH_NAME}"
    USERNAME = 'Sidbhasin13%40outlook.com'
    PASSWORD = 'helGh17aUmw3OMVHfFC5FCAF'
    JIRAURL = 'sidbhasin.atlassian.net'
  }
  stages {
    stage('Build') {
      when {
          branch 'main'
      }
      steps{
          sh(script: """
              curl -X POST https://${USERNAME}:${PASSWORD}@${JIRAURL}/rest/api/3/issue -H 'Content-Type: application/json' --data-raw '{"update": {}, "fields": {"project": {"id": "10000"},"summary": "Testing_POC_Vulnerability_Demo_2","issuetype": {"id": "10002"},"reporter": {"id": "6127263e46c81500702a010c"}}}'
            """ 
        )
      }
    }
  }
}
