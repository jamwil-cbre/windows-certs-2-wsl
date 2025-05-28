

There is a common issue to work in WSL under DPI shield. When we don't have
access to secured endpoints.

The idea is to copy ca certificates from the host Windows machine into WSL.

In Windows host machine use the suggested script `get-all-certs.ps1`
to extract all windows ca certificates in the specially created folder
`all-certificates` just in the current folder.

You can run this command in Powershell (Run as administrator) by cloning
this project and navigating to that directory to run the script with:
```
.\get-all-certs.ps1
```

Copy the crt files into `usr/local/share/ca-certificates` and
`update-ca-certificates`: 
https://documentation.ubuntu.com/server/how-to/security/install-a-root-ca-certificate-in-the-trust-store/index.html

Enjoy :)
