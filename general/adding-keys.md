# Missing GPG keys
## Problem
```
# Not the actual error, just something similar.
W: GPG error: http://ppa.launchpad.net precise 
 Release: The following signatures couldn't be verified because the public key is not available: 
 NO_PUBKEY 2EA8F35793D8809A
```

## Solution
```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys "key"
```
