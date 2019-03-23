# ALPS

[ALPS](https://dlteam.io/ALPS.pdf) is a protocol based on the Noise protocol framework.
The example echo-server/-client can be used to exchange messages according to the selected protocol-variant by ALPS:
```Noise_KK_25519_ChaChaPoly_BLAKE2s```.

Required steps:
- Clone this the repository
- [Build noise](http://rweather.github.io/noise-c/index.html)
- [Generate keys](http://rweather.github.io/noise-c/example_echo.html)

REMARK: Put the generated keys in the directories of the example echo-client/-server in order to be able to start the echo-server/-client with the following commands.

The loopback-interface will be used. TCP will be used as transport-layer-protocol.

```
// server
echo-server 7000

// client
echo-client -c client_key_25519 -s server_key_25519.pub Noise_KK_25519_ChaChaPoly_BLAKE2s 127.0.0.1 7000 
```