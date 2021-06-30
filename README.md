# Install iOS P12 certificate

Forked from: `@mobileactions/install-ios-certificate`

Run the following command to copy base64 encoded format of your p12 certificate file into your system clipboard:

```bash
base64 <P12 CERTIFICATE FILE> | pbcopy
```

Then paste it into your Github secrets.

Example: 

```
steps:
- name: Install provisioning profile
    uses: dietdoctor/install-ios-certificate@latest
    with:
        encoded-certificate: ${{ secrets.P12CERTIFICATE }}
        certificate-password: ${{ secrets.CERTIFICATE_PWD }}
        keychain: 'temp'
```