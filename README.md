Instructions:

1. Generate a new certificate

```
openssl req -x509 -newkey rsa:4096 -keyout key_enc.pem -out cert.pem -sha256 -days 365
```

2. Remove passphrase from key

```
openssl pkey -in key_enc.pem -out key.pem
```

3. Run server

```
python -m http.server 8000
```

4. Figure out your LAN IP address

On Windows, use `ipconfig` and look for IP address under a LAN section.

Then go to `<IP>:4443` on phone.
