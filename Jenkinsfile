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
input "Ready for Dev?"

milestone 21
stage "Deploy to Dev"

node {
   sh "echo deploying to dev"
}

milestone 30
input "Ready for UAT?"

milestone 31
stage "Deploy to UAT"

node {
   sh "echo deploying to UAT"
}

milestone 40
input "Ready for Prod?"

milestone 41
stage "Deploy to Prod"

node {
   sh "echo deployting to Prod"
}
