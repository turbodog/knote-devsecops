Explore devsecops with this sample application.
Full explanation of application and how to deploy it to kubernetes:
   https://learnk8s.io/nodejs-kubernetes-guide

Application includes node based web service and connected mongodb database.
Security scans depend on Prisma Cloud Compute server and twistcli from Prisma Cloud, see
    https://www.paloaltonetworks.com/resources/datasheets/prisma-cloud-at-a-glance

SETUP:
copy setupEnv_template to setupEnv and fill in values for Prisma Cloud Compute\
$ source setupEnv

STEP 1: Build insecurely
$ cd build  \
$ insecureBuildAndShare

STEP 2: Deploy insecurely (you must be connected to a kubernetes cluster)\
$ cd deploy\
$ kubectl get nodes\
$ deployApp

STEP 3: Build securely (use whatever thresholds you wish, <low, medium, high, critical>)\
        First threshold is for CVE's, second one is for compliance tolerance\
$ cd build\
$ secureBuildAndShare high high  

STEP 4:\
deploy again and see no security issues

