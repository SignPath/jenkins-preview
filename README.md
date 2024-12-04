Preview sample of [Jenkins SignPath Plugin](https://github.com/jenkinsci/signpath-plugin/)

# Preparation

1. On SignPath.io
  * Create a CI User
  * Create a TBS
  * Create a Project `Executable` for a .exe file 
  * Link the TBS in the project
  * Add a signing policy `test-signing` with the CI user as submitter
  * Add a signing policy `release-signing` with the CI user as submitter and approval process
2. Start a jenkins server with the SignPath Plugin installed

# Demo

1. Install the [Code Signing with SignPath Jenkins Plugin](https://plugins.jenkins.io/signpath/)
2. Add `SignPath.TrustedBuildSystemToken` (Scope: System) and `SignPath.ExecutableProject.ApiToken` (Scope: Global)
3. Create a new Pipeline `Sign Executable (test-signing)`
  * Add a parameter `ORGANIZATION_ID` with the org id as default
  * Select _Pipeline script from SCM_ and enter this repo URL and `Jenkinsfile.executable.test-signing` as name
4. Create a new Pipeline `Sign Executable (release-signing)`
  * Add a parameter `ORGANIZATION_ID` with the org id as default
  * Select _Pipeline script from SCM_ and enter this repo URL and `Jenkinsfile.executable.release-signing` as name
