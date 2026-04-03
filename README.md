# Operation: Hidden Leak

## Incident Overview

ACME Security Operations Center (SOC) has issued a Critical Alert. A continuous stream of sensitive company data is being exfiltrated from our production Kubernetes cluster to an unauthorized external IP address.

Internal audits confirm that the data originates from within the *'ctf'* namespace. However, the attacker was sophisticated: they haven't deployed a new pod, but instead compromised an existing, mission-critical service.

## The Constraint

You cannot stop or restart the services. These applications handle regulatory financial transactions that must remain online 24/7. Any downtime will result in severe legal penalties for the company.

## Your Mission

As a Kubernetes Expert, you have been granted access to the cluster. Your objectives are:

1. Identify the Compromised App: Locate which deployment has been hijacked to run malicious code.

2. Reverse Engineer the Entry Point: Discover how the attacker is maintaining persistence and executing their data-leak script.

3. Recover the Flag: The flag is the full name of the malicious script (including its extension) used by the attacker to automate the leak.

## Deployment Instructions

To initialize the environment and start the challenge, follow these steps. Ensure you have kubectl configured with access to your cluster (Docker Desktop, Minikube, or a remote provider).

    kubectl apply -f resources.yaml

## Validation

The flag you find is the key to the next stage of this investigation.

Flag Format: filename.extension (e.g., malware.py)

Next Step: Use the flag as the password to unlock the encrypted archive: second_mission.zip.

The clock is ticking. Every minute the script runs, more secrets leave our vault. Good luck.
