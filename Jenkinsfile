pipeline {
  agent any
  environment {
    BRANCH = "${BRANCH_NAME}"
    USERNAME = 'sidbhasin13@outlook.com'
    PASSWORD = 'RJLwvHIUJhlL6SvVT9dM1E11'
    JIRAURL = 'sidbhasin.atlassian.net'
  }
  stages {
    stage('Build') {
      when {
          branch 'main'
      }
      steps{
          sh(script: """
              curl -X POST https://${JIRAURL}/rest/api/3/issue -H 'Content-Type: application/json' 'Authorization: Basic c2lkYmhhc2luMTNAb3V0bG9vay5jb206M1hLOGgwTmd5eG84VHJiekNhSmhFNEU0' --data-raw '{"update": {}, "fields": {"project": {"id": "10000"},"summary": "Testing_POC_Vulnerability","issuetype": {"id": "10001"},"reporter": {"id": "6127263e46c81500702a010c"}}}'
            """ 
        )
      }
    }
  }
}
