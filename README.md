# Vgv-parent
Parent Maven POM

## Add GPG Key to Maven Central

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

## Add Secrets to Github
[How to add a secret to Github](https://stackoverflow.com/questions/57685065/how-to-set-secrets-in-github-actions)

Needed secrets:

* GPG_SECRET_KEY

Add this output as a value to GPG_SECRET_KEY
```
gpg --output private.key --armor --export-secret-key
```
  
* GPG_PASSPHRASE
* OSSRH_USERNAME 
* OSSRH_PASS

