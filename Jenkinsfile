stage "Build"

node {
   sh "echo building"
}

milestone 10
stage "Test"

node {
  parallel(unitTesting: {
    sh "echo unit testing"
  }, integrationTesting: {
    sh "echo integration testing"
  })
}

stage "Deploy to Dev"
milestone 20
input(message: "Ready for Dev?")
milestone 21

node {
   sh "echo deploying to dev"
   superDuperCustomStep {
        println 'Doing the super duper step'
   }
}

stage "Deploy to UAT"
milestone 30
input(message: "Ready for UAT?")
milestone 31

node {
   sh "echo deploying to UAT"
}

stage "Deploy to Prod"
milestone 40
input(message: "Ready for PROD?")
milestone 41

node {
   sh "echo deploying to Prod"
}
