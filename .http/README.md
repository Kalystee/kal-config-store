Create a file into directory '**.http**':
* filename: http-client-private.env.json
* Content:
```json
{
  "DEV": {
    "config_server_pwd": "replace_me",
    "value to encypt": "example",
    "encrypted_value": "yoyoyo"
  },
  "PROD": {
    "config_server_pwd": "replace_me",
    "value to encypt": "example",
    "encrypted_value": "yoyoyo"
  }
}
```
* Change **replace_me** by proper password
* Change **example** by the value you want to encrypt