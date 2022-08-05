pipeline {
  agent any
  environment {
    BRANCH = "${BRANCH_NAME}"
    USERNAME = 'sidbhasin13@outlook.com'
    PASSWORD = 'gbxnKh5D2Pkw4d31KoBs509A'
    JIRAURL = 'sidbhasin.atlassian.net'
  }
  stages {
    stage('Build') {
      when {
          branch 'main'
      }
      steps{
          sh(script: """
              curl -X POST https://${USERNAME}:${PASSWORD}@${JIRAURL}/rest/api/3/issue -H 'Content-Type: application/json' --data-raw '{"fields":{"project":{"id":"10001"},"key":"PV-1","issuetype":{"id":"10002"},"summary":"Testing_POC","components":[],"reporter":{"id":"6127263e46c81500702a010c"},"fixVersions":[],"assignee":{"id":"6127263e46c81500702a010c"},"priority":{"id":"3","name":"Medium"},"labels":[]},"update":{}}}'
            """ 
        )
      }
    }
  }
}
