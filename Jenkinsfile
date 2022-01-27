#!groovy

env.USER = "Kobi Shikly"
env.VERSION = "1.2.3"

basicJobParams=[
  string(name: 'param1' , defaultValue: 'first-shared-lib' , description: 'Name of shared pipeline'),
  string(name: 'param2' , defaultValue: 'main' , description: 'Name of branch'),
  string(name: 'param3' , defaultValue: 'Kobi Shikly' , description: 'User name')
]

properties([
  parameters(basicJobParams)
])			

def pipelineSharedLibrary = "${param1}@${param2}"
library changelog: false, identifier: pipelineSharedLibrary

welcomeJob.call(USER)

properties([
  buildDiscarder(logRotator(daysToKeepStr: '', numToKeepStr: '3')),
])

