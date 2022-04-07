#### Create new Private Key and Certificate Signing Request

openssl req -out domain.csr -newkey rsa:2048 -nodes -keyout domain.key

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#create-a-self-signed-certificate)Create a Self-Signed Certificate

openssl req -x509 -sha256 -nodes -newkey rsa:2048 -keyout selfsigned.key -out cert.pem
openssl req -x509 -sha256 -nodes -days 360 -newkey rsa:2048 -keyout selfsigned.key -out cert.pem

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#verify-csr-file)Verify CSR file

openssl req -noout -text -in domain.csr

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#create-rsa-private-key)Create RSA Private Key

openssl genrsa -out private.key 2048

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#remove-passphrase-from-key)Remove Passphrase from Key

openssl rsa -in certkey.key -out nopassphrase.key

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#verify-private-key)Verify Private Key

openssl rsa -in certkey.key -check

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#verify-certificate-file)Verify Certificate File

openssl x509 -in certfile.pem -text -noout

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#verify-the-certificate-signer-authority)Verify the Certificate Signer Authority

openssl x509 -in certfile.pem -noout -issuer -issuer_hash

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#check-hash-value-of-a-certificate)Check Hash Value of A Certificate

openssl x509 -noout -hash -in domain.pem

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#convert-der-to-pem-format)Convert DER to PEM format

openssl x509 -inform der -in sslcert.der -out sslcert.pem

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#convert-pem-to-der-format)Convert PEM to DER format

openssl x509 -outform der -in sslcert.pem -out sslcert.der

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#convert-certificate-and-private-key-to-pkcs12-format)Convert Certificate and Private Key to PKCS#12 format

openssl pkcs12 -export -out sslcert.pfx -inkey key.pem -in sslcert.pem

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#convert-certificate-and-private-key-to-pkcs12-format-with-chain)Convert Certificate and Private Key to PKCS#12 format with chain

openssl pkcs12 -export -out sslcert.pfx -inkey key.pem -in sslcert.pem -chain cacert.pem

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#create-csr-using-an-existing-private-key)Create CSR using an existing private key

openssl req -out certificate.csr -key existing.key -new

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#check-contents-of-pkcs12-format-cert)Check contents of PKCS12 format cert

openssl pkcs12 -info -nodes -in cert.p12

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#convert-pkcs12-format-to-pem-certificate)Convert PKCS12 format to PEM certificate

openssl pkcs12 -in cert.p12 -out cert.pem

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#test-ssl-certificate-of-particular-url)Test SSL certificate of particular URL

openssl s_client -connect yoururl.com:443 -showcerts

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#find-out-openssl-version)Find out OpenSSL version

openssl version

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#check-pem-file-certificate-expiration-date)Check PEM File Certificate Expiration Date

openssl x509 -noout -in certificate.pem -dates

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#check-certificate-expiration-date-of-ssl-url)Check Certificate Expiration Date of SSL URL

openssl s_client -connect targeturl.com:443 2>/dev/null | openssl x509 -noout -enddate

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#check-if-ssl-v2-or-v3-is-accepted-on-url)Check if SSL V2 or V3 is accepted on URL

openssl s_client -connect targeturl.com:443 -ssl2
openssl s_client -connect targeturl.com:443 -ssl3
openssl s_client -connect targeturl.com:443 -tls1
openssl s_client -connect targeturl.com:443 -tls1_1
openssl s_client -connect targeturl.com:443 -tls1_2

#### [](https://github.com/lohitakshnandan/ssl-cheat-sheet/#verify-if-the-particular-cipher-is-accepted-on-url)Verify if the particular cipher is accepted on URL

openssl s_client -cipher 'ECDHE-ECDSA-AES256-SHA' -connect targeturl:443