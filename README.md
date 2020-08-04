# CICD_Demo
Get started with Jenkins CI/CD in Red Hat OpenShift 4
#	Login to OpenShift Cluster 
oc login --insecure-skip-tls-verify --server=<Cluster URL>
#.	Create new project 
Oc new-project “kwspdemo”
#.	Create the Jenkins app
oc new-app jenkins-ephemeral
#.	Run the following command 
oc get routes
jenkins-kwspdemo.apps.shared-na4.na4.openshift.opentlc.com
                 Put that URL (jenkins-kwspdemo.apps.shared-na4.na4.openshift.opentlc.com) into your browser 

 
#.	oc create -f https://raw.githubusercontent.com/shaileshnamjoshi/CICD_Demo/master/cicd_pipeline_demo.yaml 

#.	Let’s take it for a spin
Now the magic happens. At the command line, we can run a command to see the name of the BuildConfig we want to build:

oc get buildconfigs

Want to see the pipeline? Use the following command:
	 oc get buildconfig/nodejs-sample-pipeline -o yaml

Use this command to kick off all the action:
oc start-build nodejs-sample-pipeline





