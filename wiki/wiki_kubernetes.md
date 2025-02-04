### Authentication and Authorization ###   
#### [Home](./wiki_home.md) ####
---
| STIG Number | Title | Policy | Resource |
| ----------- | ----- | ------ | -------- |
| V-242390 | The Kubernetes API server must have anonymous authentication disabled. | kas-enforce-anonymous-auth.yaml | Kubernetes STIG V2R1 |   
| V-242423 | Kubernetes etcd must enable client authentication to secure service. | NA | Kubernetes STIG V2R1 |   
| V-242424 | Kubernetes Kubelet must enable tlsPrivateKeyFile for client authentication to secure service. | NA | Kubernetes STIG V2R1 |   
| V-242425 | Kubernetes Kubelet must enable tlsCertFile for client authentication to secure service. | NA | Kubernetes STIG V2R1 |   
| V-242426 | Kubernetes etcd must enable client authentication to secure service. | NA | Kubernetes STIG V2R1 |   



### Access Control - RBAC (Role Based Access Control) ###
---
| STIG Number | Title | Policy | Resource |
| ----------- | ----- | ------ | -------- |
| V-242381 | The Kubernetes Controller Manager must create unique service accounts for each work payload. | kcm-enforce-service-account-credentials.yaml | Kubernetes STIG V2R1 |
| V-242382 | The Kubernetes API Server must enable Node,RBAC as the authorization mode. | kas-enforce-auth-mode.yaml | Kubernetes STIG V2R1 |
| V-242384 | The **Kubernetes Scheduler** must have secure binding. | ks-enforce-secure-binding.yaml | Kubernetes STIG V2R1 |
| V-242385 | The **Kubernetes Controller Manager** must have secure binding. | kcm-enforce-secure-binding.yaml | Kubernetes STIG V2R1 |  


### Network Policies ###
---
| STIG Number | Title | Policy | Resource |
| ----------- | ----- | ------ | -------- |
| V-242376 | The **Kubernetes Controller Manager** must use TLS 1.2, at a minimum, to protect the confidentiality of sensitive data during electronic dissemination. | kcm-enforce-tls.yaml | Kubernetes STIG V2R1 |  
| V-242377 | The **Kubernetes Scheduler** must use TLS 1.2, at a minimum, to protect the confidentiality of sensitive data during electronic dissemination. | ks-enforce-tls.yaml | Kubernetes STIG V2R1 |   
| V-242378 | The **Kubernetes API Server** must use TLS 1.2, at a minimum, to protect the confidentiality of sensitive data during electronic dissemination. | kas-enforce-tls.yaml | Kubernetes STIG V2R1 |
| V-242379 | The **Kubernetes etcd** must use TLS to protect the confidentiality of sensitive data during electronic dissemination. | NA | Kubernetes STIG V2R1 |
| V-242380 | The **Kubernetes etcd** must use TLS to protect the confidentiality of sensitive data during electronic dissemination. | NA | Kubernetes STIG V2R1 |   
| V-242386 | The Kubernetes API server must have the insecure port flag disabled. | kas-enforce-insecure-port.yaml (**Depreciated after v1.24**) | Kubernetes STIG V2R1 |   
| V-242388 | The Kubernetes API server must have the insecure bind address not set. | kas-enforce-insecure-bind-address.yaml | Kubernetes STIG V2R1 |    
| V-242389 | The Kubernetes API server must have the secure port set. | kas-enforce-secure-port.yaml | Kubernetes STIG V2R1 |
| V-242400 | The Kubernetes API server must have Alpha APIs disabled. | NA | Kubernetes STIG V2R1 |
| V-242404 | Kubernetes Kubelet must deny hostname override. | NA | Kubernetes STIG V2R1 |
| V-242418 | The Kubernetes API server must use approved cipher suites. | kas-enforce-cipher-suites.yaml | Kubernetes STIG V2R1 |
| V-242438 | Kubernetes API Server must configure timeouts to limit attack surface. | kas-enforce-timeouts.yaml | Kubernetes STIG V2R1 |

 

### Container/Pod Security ###
---
| STIG Number | Title | Policy | Resource |
| ----------- | ----- | ------ | -------- |  
| V-242397 | The Kubernetes kubelet staticPodPath must not enable static pods. | NA | Kubernetes STIG V2R1 | 
| V-242405 | The Kubernetes manifests must be owned by root. | NA | Kubernetes STIG V2R1 |
| V-242406 | The Kubernetes KubeletConfiguration file must be owned by root. | NA | Kubernetes STIG V2R1 |
| V-242408 | The Kubernetes manifest files must have least privileges. | NA | Kubernetes STIG V2R1 | 
| V-242409 | Kubernetes Controller Manager must disable profiling. | kcm-enforce-profiling.yaml | Kubernetes STIG V2R1 | 
| V-242434 | Kubernetes Kubelet must enable kernel protection. | NA | Kubernetes STIG V2R1 |
| V-242444 | The Kubernetes component manifests must be owned by root. | NA | Kubernetes STIG V2R1 |
| V-242445 | The Kubernetes component etcd must be owned by etcd. | NA | Kubernetes STIG V2R1 | 
| V-242446 | The Kubernetes conf files must be owned by root. | NA | Kubernetes STIG V2R1 |
| V-242449 | The Kubernetes Kubelet certificate authority file must have file permissions set to 644 or more restrictive. | NA | Kubernetes STIG V2R1 |   
| V-242450 | The Kubernetes Kubelet certificate authority must be owned by root. | NA | Kubernetes STIG V2R1 | 
| V-242451 | The Kubernetes component PKI must be owned by root. | NA | Kubernetes STIG V2R1 | 
| V-242452 | The Kubernetes Kubelet KubeConfig must have file permissions set to 644 or more restrictive. | NA | Kubernetes STIG V2R1 | 
| V-242453 | The Kubernetes Kubelet KubeConfig file must be owned by root | NA | Kubernetes STIG V2R1 |   
| V-242456 | The Kubernetes Kubelet config must have file permissions set to 644 or more restrictive. | NA | Kubernetes STIG V2R1 |   
| V-242457 | The Kubernetes Kubelet config must be owned by root. | NA | Kubernetes STIG V2R1 | 
| V-242459 | The Kubernetes etcd must have file permissions set to 644 or more restrictive. | NA | Kubernetes STIG V2R1 | 
| V-242460 | The Kubernetes admin kubeconfig must have file permissions set to 644 or more restrictive. | NA | Kubernetes STIG V2R1 |
| V-242466 | The Kubernetes PKI CRT must have file permissions set to 644 or more restrictive. | NA | Kubernetes STIG V2R1 | 
| V-245541 | Kubernetes Kubelet must not disable timeouts | NA | Kubernetes STIG V2R1 | 



### Audit Logging ###
---
| STIG Number | Title | Policy | Resource |
| ----------- | ----- | ------ | -------- |
| V-242402 | The Kubernetes API Server must have an audit log path set. | kas-enforce-audit-log-path.yaml | Kubernetes STIG V2R1 |
| V-242403 | Kubernetes API Server must generate audit records that identify what type of event has occurred, identify the source of the event, contain the event results, identify any users, and identify any containers associated with the event. | No | Kubernetes STIG V2R1 |
| V-242461 | Kubernetes API Server audit logs must be enabled. | kas-enforce-audit-logs.yaml | Kubernetes STIG V2R1 |  
| V-242462 | The Kubernetes API Server must be set to audit log max size. | kas-enforce-audit-max-size.yaml | Kubernetes STIG V2R1 |
| V-242463 | The Kubernetes API Server must be set to audit log maximum backup. | kas-enforce-audit-maxbackup.yaml | Kubernetes STIG V2R1 | 
| V-242464 | The Kubernetes API Server audit log retention must be set. | kas-enforce-audit-log-maxage.yaml | Kubernetes STIG V2R1 | 
| V-242465 | The Kubernetes API Server audit log path must be set. | kas-enforce-audit-log-path.yaml | Kubernetes STIG V2R1 | 


### Configuration Management/Resource Limitation ###
---
| STIG Number | Title | Policy | Resource |
| ----------- | ----- | ------ | -------- |
| -------- | ---------------------------------- | ----------------- | ----------------- |



### Encryption Management ###
---
| STIG Number | Title | Policy | Resource |
| ----------- | ----- | ------ | -------- |
| V-242393 | Kubernetes Worker Nodes must not have sshd service **running**. | NA | Kubernetes STIG V2R1 | 
| V-242419 | Kubernetes API Server must have the SSL Certificate Authority set. | kas-enforce-ssl-ca.yaml | Kubernetes STIG V2R1 |
| V-242420 | Kubernetes Kubelet must have the SSL Certificate Authority set. | NA | Kubernetes STIG V2R1 |
| V-242421 | Kubernetes Controller Manager must have the SSL Certificate Authority set. | kcm-enforce-ssl-ca.yaml | Kubernetes STIG V2R1 |
| V-242422 | Kubernetes API Server must have a certificate for communication. | kas-enforce-etcd-ca.yaml | Kubernetes STIG V2R1 | 
| V-242427 | Kubernetes etcd must have a key file for secure communication. | NA | Kubernetes STIG V2R1 | 
| V-242428 | Kubernetes etcd must have a certificate for communication. | NA  | Kubernetes STIG V2R1 |  
| V-242429 | Kubernetes etcd must have the SSL Certificate Authority set. | NA | Kubernetes STIG V2R1 |    
| V-242430 | Kubernetes etcd must have a certificate for communication. | NA | Kubernetes STIG V2R1 |  
| V-242431 | Kubernetes etcd must have a key file for secure communication. | NA | Kubernetes STIG V2R1 |
| V-242432 | Kubernetes etcd must have peer-cert-file set for secure communication. | NA | Kubernetes STIG V2R1 | 
| V-242433 | Kubernetes etcd must have a peer-key-file set for secure communication. | NA | Kubernetes STIG V2R1 |   
| V-245542 | Kubernetes API Server must disable basic authentication to protect information in transit. | kas-enforce-basic-auth.yaml | Kubernetes STIG V2R1 | 
| V-245543 | Kubernetes API Server must disable token authentication to protect information in transit. | kas-enforce-token-auth.yaml | Kubernetes STIG V2R1 | 
| V-245544 | Kubernetes endpoints must use approved organizational certificate and key pair to protect information in transit. | kas-enforce-endpoints.yaml | Kubernetes STIG V2R1 | 

   
   




