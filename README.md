# CI/CD Tools and Practices Final Project Template

This repository contains the template to be used for the Final Project for the Coursera course **CI/CD Tools and Practices**.

## Usage

This repository is to be used as a template to create your own repository in your own GitHub account. No need to Fork it as it has been set up as a Template. This will avoid confusion when making Pull Requests in the future.

From the GitHub **Code** page, press the green **Use this template** button to create your own repository from this template.

Name your repo: `ci-cd-final-project`.

## Setup

After entering the lab environment you will need to run the `setup.sh` script in the `./bin` folder to install the prerequisite software.

```bash
bash bin/setup.sh
```

Then you must exit the shell and start a new one for the Python virtual environment to be activated.

```bash
exit
```

## Tasks


## License

Licensed under the Apache License. See [LICENSE](/LICENSE)

## Author

Skills Network

## <h3 align="center"> © IBM Corporation 2023. All rights reserved. <h3/>

## Your task

In the terminal, install the cleanup and nose tasks by applying the tasks.yml file with kubectl apply -f .tekton/tasks.yml command.
Open the OpenShift console from the lab environment.
Create a PVC from the Administrator perspective with
storageclass: skills-network-learner
select a PVC: oc-lab-pvc
size: 1GB
Create a new pipeline and a workspace called output
Add the following steps in this order:
cleanup
git clone
flake8 linting
nose tests
buildah task
Test the pipeline works. Take a screenshot as described in this exercise's Solutions section.
Add the final step of deploying the application to the lab openshift cluster using the OpenShift client task and the oc deploy command.
oc create deployment $(params.app-name) --image=$(params.build-image) --dry-run=client -o yaml | oc apply -f -
You can refer to the videos and other content in the module CI CD with OpenShift Pipelines of the course in case you want to familiarize yourself with the concepts before proceeding further.