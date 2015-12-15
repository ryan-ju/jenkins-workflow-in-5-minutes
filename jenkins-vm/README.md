# Requirements
* Add a jdk8 tar.gz file as ./tmp/jdk.tar.gz.  This will be installed and used as the default JDK.

* Add a gpg secret key as ./tmp/secret.key.  This will be used to sign artifacts.
To export a secret key, run

```
# list keys.  02E32590 is the key ID.
$ gpg -K
/var/lib/jenkins/.gnupg/secring.gpg
-----------------------------------
sec   2048R/02E32590 2015-11-29
uid                  blah blah blah
ssb   2048R/F569ADB8 2015-11-29

# export
$ gpg --export-secret-keys -a <key_id> > secret.key
```

* Replace `your_nexus_user_name`, `your_nexus_password` and `your_gpg_key_passphrase` in ./config/settings.xml.  
The nexus values are used to upload artifacts to [Sonatype nexus](https://oss.sonatype.org), and `your_gpg_key_passphrase` should be the passphrase for ./tmp/secret.key

* (Optional) Replace `192.168.2.4` in Vagrantfile with your desired private IP
