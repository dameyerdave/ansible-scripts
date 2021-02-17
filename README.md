# Ansible scripts

## Configure SSH tunnel

```bash
Host ssh_proxy
  Hostname localhost
  Port 18183
  User tunnel
  IdentityFile ~/.ssh/tunnel

Host github.com
  ProxyJump ssh_proxy
  User git
  IdentityFile ~/.ssh/git_rsa
  AddKeysToAgent yes
```
