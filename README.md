# Your Personal OpenVPN

This template will able to help you create your own secure VPN whenever or wherever you needed it.


Steps on deploying on Azure

1. Have an Azure subscription ready.
2. Create a resource group
3. Click Add, Type in Template Deployment
2. Deploy vNet-template.
3. Deploy Azure Keyvault for your username and public key store.
    - Create a secret for your default linux admin named "linuxadmin".
    - Create a SSH RSA public key and private key using puttygen.
    - Save the private key and passphrase create for your access later upon completion of deployment.
    - Copy the public key generated and create a secret named "openvpnkey".
4. Deploy bastion-template for your remote access later (Optional).
5. Now, Deploy OpenVPN-template
    - in the adminUsername and publicKeys, replace it with the keyvault resourceId you created at step 3.
    - provide networkRG for your vNet
    - you can enable or disable autoshutdown
    
    
**Note: Provide values for solutionName, RoleName and DTAP this is for naming of your Azure Resources**
