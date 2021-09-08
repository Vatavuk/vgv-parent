# Vgv-parent
Parent Maven POM

## Add GPG Key to Github

Generate GPG key and push it to maven central server:

```
gpg --full-generate-key
```
```
gpg --list-secret-keys --keyid-format SHORT
```
```
gpg --keyserver hkp://keyserver.ubuntu.com --send-keys <key id>
```

Add gpg key as secret to github

```
gpg --output private.key --armor --export-secret-key
```

[Add GPG key to Github](https://docs.github.com/en/github/authenticating-to-github/managing-commit-signature-verification/adding-a-new-gpg-key-to-your-github-account)

## Add Secrets to Github
[How to add a secret to Github](https://stackoverflow.com/questions/57685065/how-to-set-secrets-in-github-actions)

Needed secrets:
    
* GPG_PASSPHRASE
* OSSRH_USERNAME 
* OSSRH_PASS

