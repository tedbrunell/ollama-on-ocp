# ollama-on-ocp
This repository contains yaml files for getting ollama running in OCP.

Run the  `oc apply -k ollama-llm` to deploy the resources needed to run ollama and open-webui in OpenShift.

You will want to change the `host` parameter in `open-webui-router.yaml` to match your own requirements.
