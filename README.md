# Kyverno STIG Security

## Getting started

Clone the repo using: https://github.com/1less1/kyverno-STIG-security.git

# Kyverno Policy Deployment
**2024 JCU Internship: CDTs Amber Strapponi and Dominick Olhava**  

Objective: Configure Kyverno to apply as many DISA STIGs as possible in order to secure Kubernetes and RKE2 Systems.   

[Official Kyverno Documentation](https://kyverno.io/)   
[Kyverno Policy Repo](https://github.com/1less1/kyverno-STIG-security)

This wiki will contain all documentation for applicable STIGs in the following format:  

> | STIG Number | Title | Policy | Resource |
> | ----------- | ----- | ------ | -------- |
> | V-242423 | Kubernetes etcd must enable client authentication to secure service. | NA | Kubernetes STIG V2R1 |   
> | V-242383 | User-managed resources must be created in dedicated namespaces. | require-dedicated-namespaces.yaml | Kubernetes STIG V1R11 |    
 
> ***Policy*** cells contain the name of the yaml file that will enforce the corresponding STIG or   
> NA = Not Applicable - Most likely need a bash script to verify the STIG

## Policy Template File ##
```yaml
### Policy- Template ###

# Category

# STIG Number - Title

# Other Notes

apiVersion: kyverno.io/v1
kind: ClusterPolicy
metadata:
  name: policy-name # Reflects the function of the policy and matches with the file name
  labels:
    group: cool-security-policies # Policy Group 
spec:
  validationFailureAction: Audit # or Enforce
  # Audit = Log 
  # Enforce = Deny Pod Creation
  rules:
    - name: check-if-secured # Rule Name within the Policy 
      match:
        resources:
          kinds:
            - Pod # Target Resource(s)
          names:
            - my-pod # Name of Target Pod
          namespaces:
            - my-namespace # Target Namespace 
      validate:
        message: "Error Message - Something Broken" # Error message displayed if policy is violated!
        deny: # Deny creation of pod if below requirements are not met
          conditions:
            all: 
              - key: "{{ request.object.spec.containers[].args[] }}" # Key to test against - List of arguments within pod
                operator: AllNotIn # or AnyIn 
                value: ["--audit-policy-file=/*"] # Target Value to test against the Key
                # AllNotIn - "If the value is NOT in the container DENY creation"
                # AnyIn - "If the value is IN the container DENY creation"

```



Latest DISA STIG Documentation:    
Kubernetes [V2R1](./U_Kubernetes_V2R1_STIG_SCAP_1-3_Benchmark.xml) - 15 July 2024   
RKE2 [V1R5](./U_RGS_RKE2_STIG_V1R5_Manual-xccdf.xml) - 22 April 2024 


## STIG Categories <!-- Make sure to hyperlink each page when they are created!!! -->
- [Kubernetes](./wiki/wiki_kubernetes.md)
- [RKE2](./wiki/wiki_rke2.md)<!-- Removed for sec concerns -->


