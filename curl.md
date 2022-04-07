## curl Command Options

**`curl`** accepts a wide array of options, which makes it an extremely versatile command. Options start with one or two dashes. If they do not require additional values, the single-dash options can be written together. For example, the command that utilizes the **`-O`**, **`-L`**, and **`-v`** options can be written as:

```
curl -OLv [url]
```

The list of all the available options is given below.

Option

Description

**`--abstract-unix-socket <path>`**

Connect through abstract Unix socket instead through a network.  
  
Example:  
**`curl --abstract-unix-socket socketpath https://example.com`**

**`--alt-svc <file name>`**

Enable alt-svc parser.  
  
Example:  
**`curl --alt-svc svc.txt https://example.com`**

**`--anyauth`**

Curl finds and uses the most secure authentication method for the given HTTP URL.  
  
Example:  
**`curl --anyauth --user me:pass https://example.com`**

**`-a, --append`**

Append to the target file.  
  
Example:  
**`curl --upload-file local --append ftp://example.com/`**

**`--aws-sigv4 <provider1[:provider2[:region[:service]]]>`**

Use AWS V4 signature authentication.  
  
Example:  
**`curl --aws-sigv4 "aws:amz:east-2:es" --user "key:secret" https://example.com`**

**`--basic`**

Use HTTP basic authentication.   
  
Example:  
**`curl -u name:password --basic https://example.com`**

**`--cacert <file>`**

Use the specified file for certificate verification.  
  
Example:  
**`curl --cacert CA-file.txt https://example.com`**

**`--capath <dir>`**

Use the specified directory to look for the certificates.  
  
Example:  
**`curl --capath /local/directory https://example.com`**

**`--cert-status`**

Verify the server certificate status.  
  
Example:  
**`curl --cert-status https://example.com`**

**`--cert-type <type>`**

Specify the type of the provided certificate. The recognized types are **`PEM`** (default), **`DER`**, **`ENG`** and **`P12`**.  
  
Example:  
**`curl --cert-type ENG --cert file https://example.com`**

**`-E, --cert <certificate[:password]>`**

Use the provided certificate file when working with a SSL-based protocol.  
  
Example:  
**`curl --cert certfile --key keyfile https://example.com`**

**`--ciphers <list of ciphers>`**

Provide ciphers to be used in the connection.  
  
Example:  
**`curl --ciphers ECDHE-ECDSA-AES256-CCM8 https://example.com`**

**`--compressed-ssh`**

Enable built-in SSH compression.   
  
Example:  
**`curl --compressed-ssh sftp://example.com/`**

**`--compressed`**

Request to receive a compressed response.   
  
Example:  
**`curl --compressed https://example.com`** 

**`-K, --config <file>`**

Provide a text file with curl arguments, instead of writing them on the command line.   
  
Example:  
**`curl --config file.txt https://example.com`**

**`--connect-timeout <fractional seconds>`**

Specify maximum time a curl connection may last.  
  
Example:  
**`curl --connect-timeout 30 https://example.com`**

**`--connect-to <HOST1:PORT1:HOST2:PORT2>`**

Provide a connection rule to direct requests at a specific server cluster node.   
  
Example:  
**`curl --connect-to example.com:443:example.net:8443 https://example.com`**

**`-C, --continue-at <offset>`**

Resume file transfer at the offset specified.  
  
**`curl -C 400 https://example.com`**

**`-c, --cookie-jar <filename>`**

Specify a file for storing cookies.  
  
**`curl -c store.txt https://example.com`**

**`-b, --cookie <data|filename>`**

Read cookies from a file.   
  
Example:  
**`curl -b cookiefile https://example.com`**

**`--create-dirs`**

Create the local directories for the **`--output`** option.   
  
Example:  
**`curl --create-dirs --output local/dir/file https://example.com`**

**`--create-file-mode <mode>`**

Specify which mode to set upon file creation.   
  
Example:  
**`curl --create-file-mode 0777 -T localfile sftp://example.com/new`**

**`--crlf`**

Convert LF to CRLF.   
  
**`curl --crlf -T file ftp://example.com/`**

**`--crlfile <file>`**

Provide a Certificate Revocation List for peer certificates.   
  
**`curl --crlfile revoke.txt https://example.com`**

**`--curves <algorithm list>`**

Provide curves for establishing an SSL session.  
  
Example:  
**`curl --curves X25519 https://example.com`**

**`--data-ascii <data>`**

See **`-d`**, **`--data`**.   
  
Example:  
**`curl --data-ascii @file https://example.com`**

**`--data-binary <data>`**

Post data as specified, without extra processing.   
  
**`curl --data-binary @filename https://example.com`**

**`--data-raw <data>`**

Same as **`-d`**, **`--data`**, but the @ character is not treated differently from the rest.   
  
**`curl --data-raw "@at@at@" https://example.com`**

**`--data-urlencode <data>`**

Same as **`-d`**, **`--data`**, but perform URL encoding.  
  
Example:  
**`curl --data-urlencode name=val https://example.com`**

**`-d, --data <data>`**

Send data to a HTTP server in a POST request.    
  
Example:  
**`curl -d "name=curl" https://example.com`**

**`--delegation <LEVEL>`**

Specify when the server is allowed to delegate credentials.   
  
Example:  
**`curl --delegation "always" https://example.com`**

**`--digest`**

Enable HTTP Digest authentication.   
  
Example:  
**`curl -u name:password --digest https://example.com`**

**`--disable-eprt`**

Disable EPRT and LPRT commands for active FTP transfers.   
  
Example:  
**`curl --disable-eprt ftp://example.com/`**

**`--disable-epsv`**

Disable EPSV for passive FTP transfers.  
  
Example:  
**`curl --disable-epsv ftp://example.com/`**

**`-q, --disable`**

Disable the reading of the curlrc config file.  
  
**`curl -q https://example.com`** 

**`--disallow-username-in-url`**

Exit if provided with a URL that contains a username.   
  
Example:  
**`curl --disallow-username-in-url https://example.com`**

**`--dns-interface <interface>`**

Specify an interface for outgoing DNS requests.   
  
Example:  
**`curl --dns-interface eth0 https://example.com`**

**`--dns-ipv4-addr <address>`**

Specify an IPv4 address from which the DNS requests will come.   
  
Example:  
**`curl --dns-ipv4-addr 10.1.2.3 https://example.com`**

**`--dns-ipv6-addr <address>`**

Specify an IPv6 address from which the DNS requests will come.   
  
Example:  
**`curl --dns-ipv6-addr 2a04:4e42::561 https://example.com`**

**`--dns-servers <addresses>`**

Specify your own list of DNS servers.   
  
Example:  
**`curl --dns-servers 192.168.0.1,192.168.0.2 https://example.com`**

**`--doh-cert-status`**

**`--cert-status`** for DNS-over-HTTPS.   
  
Example:  
**`curl --doh-cert-status --doh-url https://doh.server https://example.com`** 

**`--doh-insecure`**

**`-k`**, **`--insecure`** for DoH.  
  
Example:  
**`curl --doh-insecure --doh-url https://doh.server https://example.com`**

**`--doh-url <URL>`**

Specify a DoH server for hostname resolution.   
  
Example:  
**`curl --doh-url https://doh.server https://example.com`** 

**`-D, --dump-header <filename>`**

Specify a file for writing protocol headers.   
  
Example:  
**`curl --dump-header store.txt https://example.com`** 

**`--egd-file <file>`**

Provide a path for the EGD socket.   
  
Example:  
**`curl --egd-file /path/here https://example.com`** 

**`--engine <name>`**

Specify an OpenSSL crypto engine.  
  
Example:  
**`curl --engine flavor https://example.com`**  

**`--etag-compare <file>`**

Request an ETag read from a file.  
  
Example:  
**`curl --etag-compare etag.txt https://example.com`**  

**`--etag-save <file>`**

Save a HTTP ETag to a file.   
  
Example:  
**`curl --etag-save etag.txt https://example.com`** 

**`--expect100-timeout <seconds>`**

Maximum wait time for a 100-continue response.   
  
Example:  
**`curl --expect100-timeout 2.5 -T file https://example.com`** 

**`--fail-early`**

Tell curl to fail and exit when it detects the first error in transfer.   
  
Example:  
**`curl --fail-early https://example.com https://two.example`** 

**`--fail-with-body`**

If the server returns an error with code 400 or greater, curl saves the content and returns error 22.    
  
Example:  
**`curl --fail-with-body https://example.com`** 

**`-f, --fail`**

If the server returns an error, curl fails silently and returns error 22.   
  
Example:  
**`curl --fail https://example.com`** 

**`--false-start`**

Use false start on TLS handshake.   
  
Example:  
**`curl --false-start https://example.com`** 

**`--form-string <name=string>`**

Similar to **`-F`**, **`--form`**, but the value strings are processed literally.   
  
Example:  
**`curl --form-string "data" https://example.com`** 

**`-F, --form <name=content>`**

Emulate a form with a **Submit** button that has been pressed. The **`@`** sign forces the content to be a file. The **`<`** sign extracts only the content part of the file.    
  
Example:  
**`curl --form "name=curl" --form "file=@loadthis" https://example.com`**

**`--ftp-account <data>`**

Specify the account data for the FTP server.   
  
Example:  
**`curl --ftp-account "account_data" ftp://example.com/`**

**`--ftp-alternative-to-user <command>`**

Specify the command to be sent if the username and password authentication fails.   
  
Example:  
**`curl --ftp-alternative-to-user "U53r" ftp://example.com`** 

**`--ftp-create-dirs`**

If the specified directory does not exist, curl will attempt to create it.  
  
Example:  
**`curl --ftp-create-dirs -T file ftp://example.com/dirs/one/file`** 

**`--ftp-method <method>`**

Specify a method to be used for obtaining files over FTP. Available methods are **`multicwd`**, **`nocwd`**, and **`singlecwd`**.    
  
Example:  
**`curl --ftp-method multicwd ftp://example.com/dir1/dir2/file`** 

**`--ftp-pasv`**

Use passive data connection mode.   
  
Example:  
**`curl --ftp-pasv ftp://example.com/`** 

**`-P, --ftp-port <address>`**

Reverse the default roles for the FTP connection.   
  
Example:  
**`curl -P eth0 ftp:/example.com`** 

**`--ftp-pret`**

Send the PRET command before PASV/EPSV.  
  
Example:  
**`curl --ftp-pret ftp://example.com/`** 

**`--ftp-skip-pasv-ip`**

Do not use the IP address suggested by the server. curl will use the control connection IP.   
  
Example:  
**`curl --ftp-skip-pasv-ip ftp://example.com/`** 

**`--ftp-ssl-ccc-mode <active/passive>`**

Set the Clear Command Channel (CCC) mode.  
  
Example:  
**`curl --ftp-ssl-ccc-mode active --ftp-ssl-ccc ftps://example.com/`** 

**`--ftp-ssl-ccc`**

After the authentication is complete, the SSL/TLS layer is eliminated, allowing for unencrypted communication.   
  
Example:  
**`curl --ftp-ssl-ccc ftps://example.com/`** 

**`--ftp-ssl-control`**

Use SSL/TLS for logging in, stop the encryption when the data transfer starts.  
  
Example:  
**`curl --ftp-ssl-control ftp://example.com`** 

**`-G, --get`**

Use HTTP GET request instead of POST.   
  
Example:  
**`curl --get -d "tool=curl" -d "age=old" https://example.com`**

**`-g, --globoff`**

Disable the URL globbing parser.  
  
Example:  
**`curl -g "https://example.com/{[]}}}}"`**  

**`--happy-eyeballs-timeout-ms <milliseconds>`**

Use the Happy Eyeballs algorithm for connecting to dual-stack hosts.   
  
Example:  
**`curl --happy-eyeballs-timeout-ms 500 https://example.com`** 

**`--haproxy-protocol`**

Use HAProxy PROXY protocol v1 header.   
  
Example:  
**`curl --haproxy-protocol https://example.com`** 

**`-I, --head`**

Obtain only headers.  
  
Example:  
**`curl -I https://example.com`** 

**`-H, --header <header/@file>`**

Specify an additional header to be sent in the HTTP request.   
  
Example:  
**`curl -H "X-First-Name: Joe" https://example.com`** 

**`-h, --help <category>`**

See help for a specific category. **`all`** lists all the available options.   
  
Example:  
**`curl --help all`** 

**`--hostpubmd5 <md5>`**

Pass a 32-digit hexadecimal string.   
  
Example:  
**`curl --hostpubmd5 e5c1c49020640a5ab0f2034854c321a8 sftp://example.com/`** 

**`--hsts <file name>`**

Enable HSTS.   
  
Example:  
**`curl --hsts cache.txt https://example.com`** 

**`--http0.9`**

Accept a HTTP version 0.9 response.   
  
Example:  
**`curl --http0.9 https://example.com`**

**`-0, --http1.0`**

Use HTTP version 1.0.   
  
Example:  
**`curl --http1.0 https://example.com`**

**`--http1.1`**

Use HTTP version 1.1.     
  
Example:  
**`curl --http1.1 https://example.com`** 

**`--http2-prior-knowledge`**

Use HTTP version 2.0. Use this option if you know that the server supports this HTTP version.   
  
Example:  
**`curl --http2-prior-knowledge https://example.com`**

**`--http2`**

Attempt to use HTTP version 2.0.   
  
Example:  
**`curl --http2 https://example.com`**

**`--http3`**

Use HTTP version 3.0. This is an experimental option.     
  
Example:  
**`curl --http3 https://example.com`**

**`--ignore-content-length`**

Ignore the Content-Length header.  
  
Example:  
**`curl --ignore-content-length https://example.com`** 

**`-i, --include`**

Specify that the output should include the HTTP response headers.   
  
Example:  
**`curl -i https://example.com`**

**`-k, --insecure`**

Allow curl to work with insecure connections.   
  
Example:  
**`curl --insecure https://example.com`** 

**`--interface <name>`**

Specify the interface for performing an action.   
  
Example:  
**`curl --interface eth0 https://example.com`** 

**`-4, --ipv4`**

Only resolve names to IPv4 addresses.   
  
Example:  
**`curl --ipv4 https://example.com`** 

**`-6, --ipv6`**

Only resolve names to IPv6 addresses.  
  
Example:  
**`curl --ipv6 https://example.com`**

**`-j, --junk-session-cookies`**

Discard session cookies.   
  
Example:  
**`curl --junk-session-cookies -b cookies.txt https://example.com`** 

**`--keepalive-time <seconds>`**

Specify the idle time for the connection before it sends keepalive probes.   
  
Example:  
**`curl --keepalive-time 30 https://example.com`** 

**`--key-type <type>`**

Specify the type of the private key. Available types are **`PEM`** (default), **`DER`**, and **`ENG`**.   
  
Example:  
**`curl --key-type ENG --key here https://example.com`** 

**`--key <key>`**

Specify the file containing the private key.   
  
Example:  
**`curl --cert certificate --key here https://example.com`** 

**`--krb <level>`**

Enable and use Kerberos authentication. Available levels are **`clear`**, **`safe`**, **`confidential`**, and **`private`** (default).   
  
Example:  
**`curl --krb clear ftp://example.com/`** 

**`--libcurl <file>`**

Obtain C source code for the specified command line operation.   
  
Example:  
**`curl --libcurl client.c https://example.com`** 

**`--limit-rate <speed>`**

Specify the maximum upload and download transfer rate.   
  
Example:  
**`curl --limit-rate 100K https://example.com`** 

**`-l, --list-only`**

Force a name-only view.   
  
Example:  
**`curl --list-only ftp://example.com/dir/`** 

**`--local-port <num/range>`**

Specify the port numbers to be used for the connection.   
  
Example:  
**`curl --local-port 1000-3000 https://example.com`** 

**`--location-trusted`**

Similar to **`-L`**, **`--location`**, but enables you to send name and password to all redirections.  
  
Example:  
**`curl --location-trusted -u user:pass https://example.com`**

**`-L, --location`**

Allow curl to follow any redirections.   
  
Example:  
**`curl -L https://example.com`** 

**`--login-options <options>`**

Specify the login options for email server authentication.   
  
Example:  
**`curl --login-options 'AUTH=*' imap://example.com`** 

**`--mail-auth <address>`**

Provide a single address as the identity.   
  
Example:  
**`curl --mail-auth user@example.come -T mail smtp://example.com/`** 

**`--mail-from <address>`**

Provide a single "from" address.  
  
Example:  
**`curl --mail-from user@example.com -T mail smtp://example.com/`** 

**`--mail-rcpt-allowfails`**

Allows curl to continue with SMTP conversation if one of the recipients fails.   
  
Example:  
**`curl --mail-rcpt-allowfails --mail-rcpt dest@example.com smtp://example.com`** 

**`--mail-rcpt <address>`**

Provide a single "to" address.    
  
Example:  
**`curl --mail-rcpt user@example.net smtp://example.com`** 

**`-M, --manual`**

Read the curl manual.   
  
Example:  
**`curl --manual`** 

**`--max-filesize <bytes>`**

Provide the maximum size of the file to be downloaded.    
Example:  
**`curl --max-filesize 500K https://example.com`** 

**`--max-redirs <num>`**

Specify the maximum number of redirections when **`--location`** is active.   
  
Example:  
**`curl --max-redirs 3 --location https://example.com`** 

**`-m, --max-time <fractional seconds>`**

Specify the maximum time for an operation.   
  
Example:  
**`curl --max-time 5.52 https://example.com`** 

**`--metalink`**

Specify a metalink resource. This option is disabled in the newest versions of curl.   
  
Example:  
**`curl --metalink file https://example.com`** 

**`--negotiate`**

Enable SPNEGO authentication.   
  
Example:  
**`curl --negotiate -u : https://example.com`**

**`--netrc-file <filename>`**

Like **`--n`**, **`--netrc`**, but allows you to specify the file to be used.   
  
Example:  
**`curl --netrc-file netrc https://example.com`** 

**`--netrc-optional`**

Like **`--n`**, **`--netrc`**, but using netrc is optional.   
  
Example:  
**`curl --netrc-optional https://example.com`** 

**`-n, --netrc`**

Search the netrc file for login information.  
  
Example:  
**`curl --netrc https://example.com`** 

**`-:, --next`**

Use the option to separate URL requests.   
  
Example:  
**`curl -I https://example.com --next https://example.net/`** 

**`--no-alpn`**

Disable ALPN TLS extension.   
  
Example:  
**`curl --no-alpn https://example.com`** 

**`-N, --no-buffer`**

Disable output stream buffer.   
  
Example:  
**`curl --no-buffer https://example.com`** 

**`--no-keepalive`**

Disable keepalive messages.   
  
Example:  
**`curl --no-keepalive https://example.com`** 

**`--no-npn`**

Disable NPN TLS extension.   
  
Example:  
**`curl --no-npn https://example.com`** 

**`--no-progress-meter`**

Disable the progress bar but display any other message.   
  
Example:  
**`curl --no-progress-meter -o store https://example.com`** 

**`--no-sessionid`**

Disable the caching of SSL session-ID.   
  
Example:  
**`curl --no-sessionid https://example.com`** 

**`--noproxy <no-proxy-list>`**

List the hosts which should not use a proxy.   
  
Example:  
**`curl --noproxy "www.example" https://example.com`** 

**`--ntlm-wb`**

Like **`--ntlm`**, but also hands authentication to ntlmauth.  
  
Example:  
**`curl --ntlm-wb -u user:password https://example.com`**  

**`--ntlm`**

Enable NTLM authentication.   
  
Example:  
**`curl --ntlm -u user:password https://example.com`** 

**`--oauth2-bearer <token>`**

Provide a Bearer Token for OAUTH 2.0.   
  
Example:  
**`curl --oauth2-bearer "mF_9.B5f-4.1JqM" https://example.com`** 

**`--output-dir <dir>`**

Specify the output file directory.  
  
Example:  
**`curl --output-dir "tmp" -O https://example.com`** 

**`-o, --output <file>`**

Store output in a file. The output is not shown in stdout.   
  
Example:  
**`curl -o file https://example.com -o file2 https://example.net`** 

**`--parallel-immediate`**

Prefer parallel connections to waiting for new connections or multiplexed streams.   
  
Example:  
**`curl --parallel-immediate -Z https://example.com -o file1 https://example.com -o file2`**

**`--parallel-max <num>`**

Specify the maximum number of parallel connections.   
  
Example:  
**`curl --parallel-max 100 -Z https://example.com ftp://example.com/`** 

**`-Z, --parallel`**

Perform transfers in parallel.  
  
Example:  
**`curl --parallel https://example.com -o file1 https://example.com -o file2`**

**`--pass <phrase>`**

Specify a private key passphrase.   
  
Example:  
**`curl --pass secret --key file https://example.com`** 

**`--path-as-is`**

Prevent curl from merging **`/./`** and **`/../`** sequences.   
  
Example:  
**`curl --path-as-is https://example.com/../../etc/passwd`**

-**`-pinnedpubkey <hashes>`**

Specify a public key for curl to use.   
  
Example:  
**`curl --pinnedpubkey keyfile https://example.com`** 

**`--post301`**

Prevent curl from converting POST to GET requests after a 301 redirection.   
  
Example:  
**`curl --post301 --location -d "data" https://example.com`** 

**`--post302`**

Prevent curl from converting POST to GET requests after a 302 redirection.    
  
**`curl --post302 --location -d "data" https://example.com`** 

**`--post303`**

Prevent curl from converting POST to GET requests after a 303 redirection.    
  
Example:  
**`curl --post303 --location -d "data" https://example.com`** 

**`--preproxy [protocol://]host[:port]`**

Use the SOCKS proxy as a pre-proxy.   
  
Example:  
**`curl --preproxy socks5://proxy.example -x http://http.example https://example.com`** 

**`-#, --progress-bar`**

Use the simple progress bar.  
  
Example:  
**`curl -# -O https://example.com`** 

**`--proto-default <protocol>`**

Specify which protocol curl should use for URLs without a scheme name.   
  
Example:  
**`curl --proto-default https ftp.example.com`** 

**`--proto-redir <protocols>`**

Specify which protocols curl should use on redirection.   
  
Example:  
**`curl --proto-redir =http,https https://example.com`** 

**`--proto <protocols>`**

Specify which protocols curl should use for transfers.    
  
Example:  
**`curl --proto =http,https,sftp https://example.com`** 

**`--proxy-anyauth`**

Curl should choose an appropriate authentication method.   
  
Example:  
**`curl --proxy-anyauth --proxy-user user:passwd -x proxy https://example.com`**

**`--proxy-basic`**

Use HTTP Basic for communication with a proxy.   
  
Example:  
**`curl --proxy-basic --proxy-user user:passwd -x proxy https://example.com`** 

**`--proxy-cacert <file>`**

**`--cacert`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-cacert CA-file.txt -x https://proxy https://example.com`** 

**`--proxy-capath <dir>`**

**`--capath`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-capath /local/directory -x https://proxy https://example.com`**

**`--proxy-cert-type <type>`**

**`--cert-type`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-cert-type PEM --proxy-cert file -x https://proxy https://example.com`**

**`--proxy-cert <cert[:passwd]>`**

**`-E`**, **`--cert`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-cert file -x https://proxy https://example.com`** 

**`--proxy-ciphers <list>`**

**`--ciphers`** for HTTPS proxies.   
  
**`curl --proxy-ciphers ECDHE-ECDSA-AES256-CCM8 -x https://proxy https://example.com`** 

**`--proxy-crlfile <file>`**

**`--crlfile`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-crlfile rejects.txt -x https://proxy https://example.com`**

**`--proxy-digest`**

Use HTTP Digest authentication with a proxy.   
  
Example:  
**`curl --proxy-digest --proxy-user user:passwd -x proxy https://example.com`** 

**`--proxy-header <header/@file>`**

**`-H`**, **`--header`** for proxy communication.   
  
Example:  
**`curl --proxy-header "Host:" -x http://proxy https://example.com`** 

**`--proxy-insecure`**

**`-k`**, **`--insecure`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-insecure -x https://proxy https://example.com`** 

**`--proxy-key-type <type>`**

**`--key-type`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-key-type DER --proxy-key here -x https://proxy https://example.com`** 

**`--proxy-key <key>`**

**`--key`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-key here -x https://proxy https://example.com`** 

**`--proxy-negotiate`**

**`--negotiate`** for proxy communication.  
  
Example:  
**`curl --proxy-negotiate --proxy-user user:passwd -x proxy https://example.com`**

**`--proxy-ntlm`**

Use HTTP NTLM authentication with a proxy.  
  
Example:  
**`curl --proxy-ntlm --proxy-user user:passwd -x http://proxy https://example.com`**

**`--proxy-pass <phrase>`**

**`--pass`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-pass secret --proxy-key here -x https://proxy https://example.com`** 

**`--proxy-pinnedpubkey <hashes>`**

Specify the public key for proxy verification.   
  
Example:  
**`curl --proxy-pinnedpubkey keyfile https://example.com`** 

**`--proxy-service-name <name>`**

Specify the service name for proxy communciation.   
  
Example:  
**`curl --proxy-service-name "shrubbery" -x proxy https://example.com`** 

**`--proxy-ssl-allow-beast`**

**`--ssl-allow-beast`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-ssl-allow-beast -x https://proxy https://example.com`** 

**`--proxy-ssl-auto-client-cert`**

**`--ssl-auto-client-cert`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-ssl-auto-client-cert -x https://proxy https://example.com`** 

**`--proxy-tls13-ciphers <ciphersuite list>`**

Specifies the list of cipher suites to use in negotiating TLS 1.3 for proxies.   
  
Example:  
**`curl --proxy-tls13-ciphers TLS_AES_128_GCM_SHA256 -x proxy https://example.com`**

**`--proxy-tlsauthtype <type>`**

**`--tlsauthtype`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-tlsauthtype SRP -x https://proxy https://example.com`** 

**`--proxy-tlspassword <string>`**

**`--tlspassword`** for HTTPS proxies.  
  
Example:  
**`curl --proxy-tlspassword passwd -x https://proxy https://example.com`** 

**`--proxy-tlsuser <name>`**

**`--tlsuser`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-tlsuser smith -x https://proxy https://example.com`** 

**`--proxy-tlsv1`**

**`-1`**, **`--tlsv1`** for HTTPS proxies.   
  
Example:  
**`curl --proxy-tlsv1 -x https://proxy https://example.com`** 

**`-U, --proxy-user <user:password>`**

Specify the username and password for authenticating with a proxy.  
  
Example:  
**`curl --proxy-user name:pwd -x proxy https://example.com`** 

**`-x, --proxy [protocol://]host[:port]`**

Specify a proxy to use.  
  
Example:  
**`curl --proxy http://proxy.example https://example.com`** 

**`--proxy1.0 <host[:port]>`**

Specify a HTTP 1.0 proxy to use.   
  
Example:  
**`curl --proxy1.0 -x http://proxy https://example.com`** 

**`-p, --proxytunnel`**

Create a proxy tunnel.  
  
Example:  
**`curl --proxytunnel -x http://proxy https://example.com`** 

**`--pubkey <key>`**

Provide a file containing a public key.   
  
Example:  
**`curl --pubkey file.pub sftp://example.com/`** 

**`-Q, --quote <command>`**

Send a command to a FTP or SFTP server, to be executed before the transfer.   
  
Example:  
**`curl --quote "rm file" ftp://example.com/foo`** 

**`--random-file <file>`**

Specify a file containing random data. This file will be used for seeding the random engine.   
  
Example:  
**`curl --random-file rubbish https://example.com`** 

**`-r, --range <range>`**

Obtain a range of bytes.   
  
Example:  
**`curl --range 40-80 https://example.com`** 

**`--raw`**

Disable HTTP content decoding and obtain raw data.   
  
Example:  
**`curl --raw https://example.com`** 

**`-e, --referer <URL>`**

Send Referrer Page information.   
  
Example:  
**`curl --referer "https://test.example" https://example.com`** 

**`-J, --remote-header-name`**

Use header name specified by the server instead of obtaining it from the URL.  
  
Example:  
**`curl -OJ https://example.com/file`** 

**`--remote-name-all`**

Apply the **`-O`**, **`--remote-name`** option to all the URLs.  
  
Example:  
**`curl --remote-name-all ftp://example.com/file1 ftp://example.com/file2`** 

**`-O, --remote-name`**

Specify that the local file should have the name of the remote file that was downloaded.  
  
Example:  
**`curl -O https://example.com/filename`** 

**`-R, --remote-time`**

Specify that the local file should have the timestamp of the remote file that was downloaded.  
  
Example:  
**`curl --remote-time -o foo https://example.com`** 

**`--request-target <path>`**

Specify an alternative target path.  
  
Example:  
**`curl --request-target "*" -X OPTIONS https://example.com`** 

**`-X, --request <command>`**

Specify a request method for communication with the server.  
  
Example:  
**`curl -X "DELETE" https://example.com`** 

**`--resolve <[+]host:port:addr[,addr]...>`**

Specify a custom address for a host/port.   
  
Example:  
**`curl --resolve example.com:443:127.0.0.1 https://example.com`** 

**`--retry-all-errors`**

Force retrying on all errors.  
  
Example:  
**`curl --retry-all-errors https://example.com`** 

**`--retry-connrefused`**

Add ECONNREFUSED to the list of errors that are eligible for **`--retry`**.   
  
Example:  
**`curl --retry-connrefused --retry https://example.com`** 

**`--retry-delay <seconds>`**

Specify the amount of time between retries.   
  
Example:  
**`curl --retry-delay 5 --retry https://example.com`** 

**`--retry-max-time <seconds>`**

Specify the maximum amount of time for **`--retry`** attempts.   
  
Example:  
**`curl --retry-max-time 30 --retry 10 https://example.com`** 

**`--retry <num>`**

Specify the number of retries after curl encounters and error.   
  
Example:  
**`curl --retry 7 https://example.com`**

**`--sasl-authzid <identity>`**

Specify an additional authentication identity for SASL PLAIN authentication.   
  
Example:  
**`curl --sasl-authzid zid imap://example.com/`** 

**`--sasl-ir`**

Enable initial response during SASL authentication.  
  
Example:  
**`curl --sasl-ir imap://example.com/`** 

**`--service-name <name>`**

Specify the SPNEGO service name.   
  
Example:  
**`curl --service-name sockd/server https://example.com`** 

**`-S, --show-error`**

Show an error message event with the **`-s`**, **`--silent`** option enabled.   
  
Example:  
**`curl --show-error --silent https://example.com`** 

**`-s, --silent`**

Turn on the silent mode. This option mutes curl.  
  
Example:  
**`curl -s https://example.com`** 

**`--socks4 <host[:port]>`**

Specify a SOCKS4 proxy.  
  
Example:  
**`curl --socks4 hostname:4096 https://example.com`** 

**`--socks4a <host[:port]>`**

Specify a SOCKS4a proxy.   
  
Example:  
**`curl --socks4a hostname:4096 https://example.com`** 

**`--socks5-basic`**

Use the basic authentication method (username/password) with a SOCKS5 proxy.   
  
Example:  
**`curl --socks5-basic --socks5 hostname:4096 https://example.com`** 

**`--socks5-gssapi-nec`**

Allow protection mode negotiation to be unprotected.  
  
Example:  
**`curl --socks5-gssapi-nec --socks5 hostname:4096 https://example.com`** 

**`--socks5-gssapi-service <name>`**

Change the name of a socks server.  
  
Example:  
**`curl --socks5-gssapi-service sockd --socks5 hostname:4096 https://example.com`** 

**`--socks5-gssapi`**

Use GSS-API authentication with a SOCKS5 proxy.   
  
Example:  
**`curl --socks5-gssapi --socks5 hostname:4096 https://example.com`** 

**`--socks5-hostname <host[:port]>`**

Specify the SOCKS5 proxy to use.   
  
Example:  
**`curl --socks5-hostname proxy.example:7000 https://example.com`** 

**`--socks5 <host[:port]>`**

Specify the SOCKS5 proxy to use. The hostname is resolved locally.   
  
Example:  
**`curl --socks5 proxy.example:7000 https://example.com`** 

**`-Y, --speed-limit <speed>`**

Set the lower limit for the download speed.  
  
Example:  
**`curl --speed-limit 300 --speed-time 10 https://example.com`** 

**`-y, --speed-time <seconds>`**

Set the time period for the speed limit measurement.   
  
Example:  
**`curl --speed-limit 300 --speed-time 10 https://example.com`** 

**`--ssl-allow-beast`**

Tell curl to ignore the BEAST security flaw in the SSL3 and TLS1.0 protocols.   
  
Example:  
**`curl --ssl-allow-beast https://example.com`** 

**`--ssl-auto-client-cert`**

Obtain and use a client certificate automatically.   
  
Example:  
**`curl --ssl-auto-client-cert https://example.com`** 

**`--ssl-no-revoke`**

Do not check for certificate revocation.   
  
Example:  
**`curl --ssl-no-revoke https://example.com`** 

**`--ssl-reqd`**

Require SSL/TLS.   
  
Example:  
**`curl --ssl-reqd ftp://example.com`** 

**`--ssl-revoke-best-effort`**

Ignore certificate revocation checks if they failed because of missing distribution points.  
  
Example:  
**`curl --ssl-revoke-best-effort https://example.com`** 

**`--ssl`**

Attempt to use SSL.   
  
Example:  
**`curl --ssl pop3://example.com/`** 

**`-2, --sslv2`**

Use SSLv2. Newer curl versions ignore this request due to security concerns with SSLv2.  
  
Example:  
**`curl --sslv2 https://example.com`** 

**`-3, --sslv3`**

Use SSLv3. Newer curl versions ignore this request due to security concerns with SSLv3.    
  
Example:  
**`curl --sslv3 https://example.com`** 

**`--stderr <file>`**

Output stderr to a file. The **`-`** symbol tells curl to output stderr to stdout.   
  
Example:  
**`curl --stderr output.txt https://example.com`** 

**`--styled-output`**

Enable bold fonts for HTTP header terminal output.   
  
**`curl --styled-output -I https://example.com`** 

**`--suppress-connect-headers`**

Prevent curl from outputting CONNECT headers.   
  
Example:  
**`curl --suppress-connect-headers --include -x proxy https://example.com`** 

**`--tcp-fastopen`**

Enable TCP Fast Open.  
  
Example:  
**`curl --tcp-fastopen https://example.com`**

**`--tcp-nodelay`**

Enable TCP_NODELAY.   
  
Example:  
**`curl --tcp-nodelay https://example.com`** 

**`-t, --telnet-option <opt=val>`**

Pass the **`TTYPE`**, **`XDISPLOC`**, and **`NEW_ENV`** options to the telnet protocol.   
  
Example:  
**`curl -t TTYPE=vt100 telnet://example.com/`** 

**`--tftp-blksize <value>`**

Set the value of TFTP BLKSIZE. Must be a value larger than 512.   
  
Example:  
**`curl --tftp-blksize 1024 tftp://example.com/file`** 

**`--tftp-no-options`**

Prevents curl from sending requests for TFTP options.  
  
Example:  
**`curl --tftp-no-options tftp://192.168.0.1/`** 

**`-z, --time-cond <time>`**

Request a document that was modified after a certain date and time. For documents modified before the time, prefix the date expression with a dash.  
   
Example:  
**`curl -z "Wed 01 Sep 2021 12:18:00" https://example.com`** 

**`--tls-max <VERSION>`**

Specify the newest TLS version that is supported.  
  
Example:  
**`curl --tls-max 1.2 https://example.com`** 

**`--tls13-ciphers <ciphersuite list>`**

Specifies the list of cipher suites to use in negotiating TLS 1.3    
  
Example:  
**`curl --tls13-ciphers TLS_AES_128_GCM_SHA256 https://example.com`** 

**`--tlsauthtype <type>`**

Specify the TLS authentication type.  
  
Example:  
**`curl --tlsauthtype SRP https://example.com`** 

**`--tlspassword <string>`**

Specify the TLS password.   
  
Example:  
**`curl --tlspassword pwd --tlsuser user https://example.com`** 

**`--tlsuser <name>`**

Specify the TLS username.   
  
Example:  
**`curl --tlspassword pwd --tlsuser user https://example.com`** 

**`--tlsv1.0`**

Tell curl to use TLS1.0 or newer.   
  
Example:  
**`curl --tlsv1.0 https://example.com`** 

**`--tlsv1.1`**

Tell curl to use TLS1.1 or newer.    
  
Example:  
**`curl --tlsv1.1 https://example.com`** 

**`--tlsv1.2`**

Tell curl to use TLS1.2 or newer.    
  
Example:  
**`curl --tlsv1.2 https://example.com`** 

**`--tlsv1.3`**

Tell curl to use TLS1.3 or newer.    
  
Example:  
**`curl --tlsv1.3 https://example.com`** 

**`-1, --tlsv1`**

Specify that curl should use at least 1.x version of TLS.  
  
Example:  
**`curl --tlsv1 https://example.com`** 

**`--tr-encoding`**

Ask for a compressed Transfer-Encoding response.  
  
Example:  
**`curl --tr-encoding https://example.com`** 

**`--trace-ascii <file>`**

Enable a full trace dump to a file. Eliminates the hex part and shows only ASCII.  
  
Example:  
**`curl --trace-ascii log.txt https://example.com`** 

**`--trace-time`**

Require a time stamp on each trace or verbose line.   
  
Example:  
**`curl --trace-time --trace-ascii output https://example.com`** 

**`--trace <file>`**

Enable a full trace dump to a file.    
  
Example:  
**`curl --trace log.txt https://example.com`** 

**`--unix-socket <path>`**

Specify a Unix socket path.   
  
Example:  
**`curl --unix-socket socket-path https://example.com`** 

**`-T, --upload-file <file>`**

Upload a file to the URL.   
  
Example:  
**`curl -T "img[1-1000].png" ftp://ftp.example.com/`** 

**`--url <url>`**

Provide a URL to be fetched.   
  
Example:  
**`curl --url https://example.com`** 

**`-B, --use-ascii`**

Enable ASCII transfer.   
  
Example:  
**`curl -B ftp://example.com/README`** 

**`-A, --user-agent <name>`**

Specify the user agent name.   
  
Example:  
**`curl -A "Agent 007" https://example.com`** 

**`-u, --user <user:password>`**

Provide the username and password for authentication.   
  
Example:  
**`curl -u user:secret https://example.com`** 

**`-v, --verbose`**

Tell curl to be verbose.   
  
Example:  
**`curl --verbose https://example.com`** 

**`-V, --version`**

See the installed versions of curl and libcurl.  
  
Example:  
**`curl --version`** 

**`-w, --write-out <format>`**

Tell curl to show information about the completed transfer on stdout.   
  
Example:  
**`curl -w '%{http_code}\n' https://example.com`** 

**`--xattr`**

Store file metadata in file attributes.  
  
Example:  
**`curl --xattr -o storage https://example.com`**








*source*
[https://phoenixnap.com/kb/curl-command#:~:text=apt%20install%20curl-,What%20Is%20the%20curl%20Command%3F,to%20be%20sent%20or%20received.]()