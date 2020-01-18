Explore devsecops with this sample application.

STEP 1: Build insecurely.
$ cd build
$ insecureBuildAndShare mongo 1

STEP 2: Deploy insecurely (you must be connected to kubernetes cluster)
$ cd deploy
$ kubectl get nodes`
$ deployApp

STEP 3: Build securely
$ cd build
$ secureBuildAndShare bitname/mongodb 2  

STEP 4:
deploy again and see no security issues

