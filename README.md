# Welcome to the innovatie-helm-charts Github page

This project is in collaboration with VIVES University of applied sciences. It collects data from TABS motion sensors and uses a python-program to write the data to an influx database and retrieve it again in use of the API. 

The purpose of this page is to be a specific URL to the github repository so that it can be used in artifacthub. 
Artifacthub ensures that our product can be easily deployed in kubernetes clusters using the `helm install` command

**Our artifacthub-page can be found here:**

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/motion-sensors)](https://artifacthub.io/packages/search?repo=motion-sensors)

## Contents

### Chart.yaml

This is the explanation yaml-file for the project. this contains the name, version and description of the code.

### values.yaml

This file contains everything needed for the deployment and setup only, in the kubernetes cluster. If the hostport or image needs to be changes, this is where it would be done.

### ./templates

Templates contain the files for the actual depoyment of the service.

1. Configmap.yaml: All enviroment variables that aren't confidential are stored here for use in the cluster.
2. Secret.yaml: All environment variables that ***are*** confidential are loaded into and contained within this file.
3. Deployment.yaml: This specifies the container in which our app is used. Do not change this file.
4. Service.yaml: Configures the service based on the deployment.
5. The remainder of the files aren't that important to the correct working of the service.

## Support or Contact

Due to this being a private project, there is no possibility to have any support for the project nor have any contact with the creators of this project.
