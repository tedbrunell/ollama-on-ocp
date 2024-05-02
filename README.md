# ollama-on-ocp
This repository contains yaml files for getting ollama running in OCP.  They have been tested in a Single Node OpenShift (SNO) installation.

Run the  `oc apply -k ollama-llm` to deploy the resources needed to run ollama and open-webui in OpenShift.

You will want to change the `host` parameter in `open-webui-router.yaml` to match your own requirements.

##NOTE: you will need to ensure that you have persistent storage and that the `lvms-vg1` storage class is set to default.  That can be accomplished with the following OC command:

``oc patch storageclass lvms-vg1 -p '{"metadata": {"annotations": {"storageclass.kubernetes.io/is-default-class": "true"}}}'``
