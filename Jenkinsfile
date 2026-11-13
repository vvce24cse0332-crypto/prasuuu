pipeline{
 agent any
stages {

stage('Checkout') {
steps  {
checkout scm
}
}
stage(Build')  {
steps{
echo "Checking Python application'
bat 'python -m py_compile app.py'
}
}
stage('Test')  {
steps {
echo 'Executing automated tests'
bat 'python -m unittest app'
}
}
stage("Run Apllication')  {
steps {
bat 'python app.py'
}
}
}
post{
success {
echo 'CII Pipeline completed successfully'
}
failure {
echo "CI Pipeline failed'
}
}
}
