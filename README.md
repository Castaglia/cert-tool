cert-tool
=========

Synopsis
--------
This `cert-tool` Perl script provides command-line options for generating
certs/keys using the OpenSSL command-line tools and config file.

For further module documentation, see cert-tool.html.

Usage
-----
Commands for creating a CA, server certificate, and client certificate:

    $ ./cert-tool --create-ca=myca --combined \
        --signing-ca=self

    $ ./cert-tool --create-cert=myserver --combined \
        --signing-ca=myca.pem --signing-key=myca.pem

    $ ./cert-tool --create-cert=myclient --combined \
        --signing-ca=myca.pem --signing-key=myca.pem

That's it.  You should now have your certificates _combined_ with their
private keys into PEM files: `myca.pem`, `myserver.pem`, and `myclient.pem`.
