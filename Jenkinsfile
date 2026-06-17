pipeline{
agent any
tools{
maven 'maven'
}
stages{
stage('Checkout'){
steps{
git branch:'master',url:'https://github.com/Langerraghav12/seli.git'
}}
stage('Build'){
steps{
sh 'mvn clean package'
}}
stage('Test'){
steps{
sh 'mvn test'
}}
stage('Run'){
steps{
sh 'mvn clean install '
}}}
post{
success{
echo 'Open SauceDemo: https://www.saucedemo.com'
}
failure{
echo 'Build failed'
}}}
