pipeline {
	agent any
	stages {
		stage("dotnet restore") {
			when {
				branch 'main'
			}
			steps {
				sh "dotnet restore"
			}
		}
		stage("dotnet build") {
			when {
				branch 'main'
			}
			steps {
				sh "dotnet build --no-restore"
			}
		}
		stage("dotnet test") {
			when {
				branch 'main'
			}
			steps {
				sh "dotnet test --no-build"
			}
		}
	}
}

