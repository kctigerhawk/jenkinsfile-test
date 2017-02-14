stage "Build"

node {
   sh "echo building"
}

milestone 10
stage "Test"

node {
  parallel (unitTesting: {
    sh "echo unit testing"
  }, integrationTesting: {
    sh "echo integration testing"
  })
}

milestone 20
input message: "Ready for Dev?", ok: "Go?", submitter: "developer"

milestone 21
stage "Deploy to Dev"

node {
   sh "echo deploying to dev"
}

milestone 30
input message: "Ready for UAT?", submitter: "approver"

milestone 31
stage "Deploy to UAT"

node {
   sh "echo deploying to UAT"
}

milestone 40
input message: "Ready for PROD?", submitter: "approver"

milestone 41
stage "Deploy to Prod"

node {
   sh "echo deployting to Prod"
}
