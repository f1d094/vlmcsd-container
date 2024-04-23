# Containerized vlmcsd

***VLMCSD*** is a free, open-source software to provide an activation service (KMS) for any computer using Windows products

## Container:
https://hub.docker.com/repository/docker/f1d094/vlmcsd

## Server Usage:
> $ docker run -d 1688:1688 --restart=always --name vlmcsd f1d094/vlmcsd

## Examples
### Operating System
>slmgr.vbs -upk  
>slmgr.vbs -ipk XXXXX-XXXXX-XXXXX-XXXXX-XXXXX  
>slmgr.vbs -skms CONTAINER_IP:PORT  
>slmgr.vbs -ato  
>slmgr.vbs -dlv  

### Office
>cd \Program Files\Microsoft Office\Office16  
>cscript ospp.vbs /sethst:CONTAINER_IP  
>cscript ospp.vbs /setprt:PORT  
>cscript ospp.vbs /inpkey:xxxxx-xxxxx-xxxxx-xxxxx-xxxxx  
>cscript ospp.vbs /act  
>cscript ospp.vbs /dstatusall  

## GVLK lookup
> Operating Systems:
> https://learn.microsoft.com/en-us/windows-server/get-started/kms-client-activation-keys
> Office, Project, and Visio:
> https://learn.microsoft.com/en-us/DeployOffice/vlactivation/gvlks

## Source
> https://github.com/tfslabs/vlmcsd

