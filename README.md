Explore devsecops with this sample application.
Full explanation of application and how to deploy it to kubernetes:
   https://learnk8s.io/nodejs-kubernetes-guide

Application includes node based web service and connected mongodb database.
Security scans depend on Prisma Cloud Compute server and twistcli from Prisma Cloud, see
    https://www.paloaltonetworks.com/resources/datasheets/prisma-cloud-at-a-glance

STEP 1: Build insecurely (version 1).
$ cd build 
$ insecureBuildAndShare mongo 1

STEP 2: Deploy insecurely (you must be connected to a kubernetes cluster)
$ cd deploy
$ kubectl get nodes`
$ deployApp

STEP 3: Build securely
$ cd build
$ secureBuildAndShare bitname/mongodb 2  

STEP 4:
deploy again and see no security issues

