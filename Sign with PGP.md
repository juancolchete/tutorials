```
sudo apt-get install gnupg
```

```sh
gpg --gen-key
```

```sh
gpg --sign-key example@example.com
```

```sh
gpg --fingerprint example@example.com
```

```sh
gpg --send-keys --keyserver pgp.mit.edu key_id
```

```sh
gpg --encrypt --sign --armor -r example@example.com name_of_file
```
