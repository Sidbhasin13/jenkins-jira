pipeline {
  agent any
  environment {
    BRANCH = "${BRANCH_NAME}"
    USERNAME = 'sidbhasin13@outlook.com'
    PASSWORD = '3XK8h0Ngyxo8TrbzCaJhE4E4'
    JIRAURL = 'sidbhasin.atlassian.net'
  }
  stages {
    stage('Build') {
      when {
          branch 'main'
      }
      steps{
          sh(script: """
              curl -X POST https://${USERNAME}:${PASSWORD}@${JIRAURL}/rest/api/3/issue -H 'Content-Type: application/json' --data-raw '{"update": {}, "fields": {"project": {"id": "10000"},"summary": "Testing_POC_Vulnerability_Airtel","issuetype": {"id": "10001"},"reporter": {"id": "6127263e46c81500702a010c"}}}'
            """ 
        )
      }
    }
  }
}
