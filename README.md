# SIP Vs WEBRTC (Secure Voice Communication) 

A comparison of SIP and WEBRTC protocols will be shown in terms of performance and speed


## SIP

### OPENSSL
OpenSSL 1.1.1k Supports AES-GCM that's why we are going to use this version to be able to encrypt voice data so in terms of this project SRTP packets will be used instead of RTP.

```bash
wget https://github.com/openssl/openssl/archive/refs/tags/OpenSSL_1_1_1k.zip
```

```bash
./config
```
This will show to you:
> Operating system: x86_64-whatever-linux2

```bash
./Configure x86_64-whatever-linux2
```

```bash
make -j4
```
### PJSIP
To be able to create sip client in this project [pjsip](https://github.com/pjsip/pjproject) sip stack will be used. Clone it and follow the steps.


> Edit pjsua2-demo file according to following line

```bash
nano <pj-path>/pjsip-apps/src/samples/pjsua2_demo.cpp 
```

```bash
./configure --with-ssl=<PATH_OF_BUILT_OPENSSL>
```
```bash
make dep && make clean && make -j4
```
> <pj-path>/pjsip-apps/bin/samples/x86_64-unknown-linux-gnu can be used as sip client.



## WEBRTC
### THIS PART WILL BE WRITTEN LATER...

## Usage
This part will be written later.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
