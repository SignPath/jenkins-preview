Preview sample of [Jenkins SignPath Plugin](https://github.com/jenkinsci/signpath-plugin/)

# Preparation

1. On SignPath.io
  * Create a CI User
  * Create a TBS
  * Create a Project `Executable` for a .exe file 
  * Link the TBS in the project
  * Add a signing policy `test-signing` with the CI user as submitter
2. Start a jenkins server with the SignPath Plugin installed
  * See the [documentation](https://about.signpath.io/documentation/trusted-build-systems/jenkins) for the setup
3. Create a new Pipeline `Sign Executable (test-signing)`
  * Select _Pipeline script from SCM_ and enter this repo URL and `Jenkinsfile.executable.test-signing` as name
