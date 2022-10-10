# How to use self-signed Root certificate on iOS Mobile

Communicate to a server from mobile apps, Mobile devices will work only with a public CA-signed certificate server by default. However, We can disable the SSL check to communicate with servers that are using self-signed certificates but it will lead to a security vulnerability. hence, we are supporting only the public CA-signed certificate holding servers.

Whereas for some development process we are bound to help to access the self-signed certificate connections hence we are providing a workaround to use a self-signed certificate in iPhone, The procedure how to create a root self-signed certificate and install in iPhones given below.

The very first and most important point is generating the proper root self-signed certificate, The steps to create a self-signed certificate are,

### Create a Root Key

**Attention:** this is the key used to sign the certificate requests, anyone holding this can sign certificates on your behalf. So keep it in a safe place!

> openssl genrsa -des3 -out rootCA.key 4096

If you want a non-password protected key just remove the -des3 option

### Create and self sign the Root Certificate

> openssl req -x509 -new -nodes -key rootCA.key -sha256 -days 1024 -out rootCA.crt /CN=mydomain.com

Here we used our root key to create the root certificate that needs to be distributed in all the computers that have to trust us.

### Convert the .crt certificate to  .pfx

Servers will understand only .pfx formate of the certificate hence we need to convert the .crt formate to .pfx below command used to convert the same

> openssl pkcs12 -export -out certificate.pfx -inkey rootCA.key -in rootCA.crt

Once the certificate is installed in the server then the same .crt certificate should be installed on the phone as well

### Install the self-signed .crt certificate in iPhone

First, email your root certificate (e.g. rootCA.crt) to yourself (Email must be default iPhone mail app not like other Gmail or outlook app).



Next, open the email on your phone, and click the attachment. This will open the iOS Setting up and offer you to install the certificate as a Profile.

If the phone is in the latest iOS then it will download the profile and keep in setting app whereas in the older OS after downloading the certificate it will directly open the setting app to install the certificate.



If its latest OS then, once the profile is downloaded open the setting app and navigate to General → Profile & Device Management



Open the downloaded certificate



Install the certificate. Once the installation is done then it will show the verified indicator which tells the certificate installation proper and successful.



After installing the certificate the important step is trusting the certificate otherwise iPhone will not use this certificate, for that

Navigate to Settings app → General → About → Certificate Trust Settings



Once the certificate is trusted then open the Archer Web Application in Safari to make sure the certificate is working properly.

If the Safari is able to open the Archer Web without any error then we are good to use the Archer App as well.

### Useful Links

https://medium.com/collaborne-engineering/self-signed-certificates-in-ios-apps-ff489bf8b96e

https://gist.github.com/iansheridan/62a53a8675ad3f415e5e

https://stackoverflow.com/questions/49422164/how-to-install-self-signed-certificates-in-ios-11/52520343#52520343

https://stackoverflow.com/questions/6307886/how-to-create-pfx-file-from-certificate-and-private-key

### General Issues
Some time if the certificate is not a proper root certificate then while installing on phone  it won't appear in the trusted area where we have to trust the certificate
While creating the certificate we have to provide the same domain name /CN=mydomain.com otherwise OS can't match the certificate with the hostname hence OS won't recognize the certificate which comes from the server


