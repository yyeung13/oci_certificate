# OCI Certificate
This repository explains how to create and use Certificate Authority and Certificate in OCI<br>
<br>
(WIP) More details to be provided in the future<br>
<br>
Step 1: Configure IAM Policy in OCI<br>
<br>
For a jumpstart, make sure the following policies are configured:<br>
<br>
<pre>
  Allow service certificates to use keys in compartment yy
  Allow service certificates to use vaults in compartment yy
  Allow any-group to manage keys in compartment yy
  Allow any-group to manage vaults in compartment yy
  Allow dynamic-group CertificateAuthority-DG to use keys in compartment yy
  Allow dynamic-group CertificateAuthority-DG to manage objects in compartment yy
  Allow any-group to manage all-resources in compartment yy
</pre>
Replace 'yy' with your compartment id.<br>
<br>
Step 2: Configure Vault<br>
OCI Certificate Authority and Certificate require Vault to be configured first<br>
<br>
Note that the vault should use HSM instead of software<br>
Also setup a Hardware RSA Key and a secret as well<br>
Step 3: Generate Certificate Authority<br>
<br>
Step 4: Generate Certificate<br>
<br>
Step 5: Download Key and Certificate<br>
<br>
Note that certificate private key can't be downloaded from OCI console, use this to download from CLI<br>
<pre>
  oci certificates certificate-bundle get --certificate-id <certificate-ocid> --bundle-type CERTIFICATE_CONTENT_WITH_PRIVATE_KEY > bundle.json
</pre>

