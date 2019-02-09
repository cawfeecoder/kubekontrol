# kubekontrol
![Architecture](/architecture.png)
KubeKontrol is an ambitious project to provide authorization and authentication for Kubernetes clusters through the use of policies and X509 certificates. In particular, kubekontrol enables the following:
* Authentication of users using X509 issued certificates
* Authorization based on Common Name (CN) lookup, Certification Revocation List (CRL) checks, and RBAC, ABAC, and ACL policies powered by Open Policy Agent (OPA)
* Dynamically change policies on the fly without restarting

Notice, we provide an architectural overview in which we see kubekontrol working. In particular, kubekontrol will expect particular X-SSL headers in order to provide decisions. There will exist configuration (optionally) to utilize the serial and check the Certification Revocation List (CRL) to ensure users are still authorized. We also will enable (optionally) to dynamically provisioning and revoke certificates by using a third party provider (i.e. Vault). Finally, we will also allow (optionally) the ability to read and display Kubernetes Audit Logs. At this time, we are unsure if we are providing a compliant Audit Backend via WebHook in order to provide this functionality.
