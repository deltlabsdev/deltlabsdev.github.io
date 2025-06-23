# SQL LRS

SQL LRS is an Apache 2.0 open source xAPI Learning Record Store from Yet Analytics. 

## Windows Installation

1. Download files from https://github.com/yetanalytics/lrsql/releases.
2. Unzip files to folder on your computer.
3. Open config folder and copy lrsql.json.example to lrsql.json. Set user name and password.
4. Run lrsql.exe. If you get the "Windows protected your PC" message, click on "More info" and "Run anyway".
5. Open http://localhost:8080/admin.

## HTTPS on Windows

For testing, the default HTTP connection works fine. For some use cases a HTTPS connection to the Learning Record Store is required. You can self-issue a certificate for SQLLRS:

1. Open PowerShell as Administrator.
2. Run
    ```json
   New-SelfSignedCertificate -CertStoreLocation Cert:\LocalMachine\My -DnsName “localhost” -FriendlyName “MyLocalSiteCert” -NotAfter (Get-Date).AddYears(10)
   ```
   You can choose any string as friendly name.
3. Login as Administrator.
4. Run “Manage computer certificates” from Start.
5. Drag and drop the new certificate form Personal – Certificates folder into the Trusted Root Certification Authorities – Certificates folder.
6. Double click on the certificate.
7. Go to "Details" and click "Copy to file".
8. Export the file as a PFX file into your SQLLRS config folder. If you have Git installed on your computer, run openssl.exe from the Git folder. 
   Run these commands from your SQLLRS config folder:
   ```json
   C:\Users\...\AppData\Local\Programs\Git\usr\bin\openssl.exe pkcs12 -in localcert.pfx -nocerts -out localcert.key.pem -nodes
   C:\Users\...\AppData\Local\Programs\Git\usr\bin\openssl.exe pkcs12 -in localcert.pfx -clcerts -nokeys -out localcert.crt.pem
   ```json
9. Add the certificates to the config file.

After adding the pem files and updating the configuration file as below, you should be able to open the LRS Administration with a secure connection from your browser (
https://localhost:8443/admin).


```json
{  
  "lrs" : {
    "adminUserDefault": "admin",
    "adminPassDefault": "lrs",
    "authorityUrl": "http://deltlabs.com",
    "enableReactions": true
  },  
  "webserver": {
    "httpHost": "0.0.0.0",
    "httpPort": 8081,
    "sslPort": 8443,
    "allowAllOrigins": true,
    "keyPkeyFile" : "config/localcert.key.pem",
    "keyCertChain" : "config/localcert.crt.pem"
  }
}
```



