# CICD_Demo
Get started with Jenkins CI/CD in Red Hat OpenShift 4
1.	Login to OpenShift Cluster 
oc login --insecure-skip-tls-verify --server=<Cluster URL>
2.	Create new project 
Oc new-project “kwspdemo”
3.	Create the Jenkins app
oc new-app jenkins-ephemeral
4.	Run the following command 
oc get routes
jenkins-kwspdemo.apps.shared-na4.na4.openshift.opentlc.com
                 Put that URL (jenkins-kwspdemo.apps.<cluster_url>) into your browser 

 
5.	oc create -f https://raw.githubusercontent.com/shaileshnamjoshi/CICD_Demo/master/cicd_pipeline_demo.yaml 

6.	Let’s take it for a spin
Now the magic happens. At the command line, we can run a command to see the name of the BuildConfig we want to build:

7.   oc get buildconfigs

8. Want to see the pipeline? Use the following command:
  oc get buildconfig/nodejs-sample-pipeline -o yaml

9. Use this command to kick off all the action:
  oc start-build nodejs-sample-pipeline







