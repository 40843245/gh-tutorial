# gh
## command
### auth
#### login

+ How to login Github account in GitBash.

One way is to use gh, the command is `gh auth login`.

Follow these steps:

1. In GitBash, type `gh auth login`.
2. Choose the `account` that you want to log into.
3. Choose the preferred `protocol` for Git operations on this host.
4. Either 
   + create a SSH public key (if it does NOT exist on local device, by default it is under the directory `C:\Users\{USERNAME}\.ssh`).
   + choose to upload or NOT (if it DOES exist on local device).
5. Choose the option to authenticate GitHub CLI.
6. In above step, if you choose the option `Paste an authentication token`. Do the following:
   1. Generate a new token at `https://github.com/settings/tokens`.
      > [!IMPORTANT]
      > At present, Github requires the new token must have at these scopes:
      > + `repo`
      > + `read:org`
   2. Copy the new token.
      > [!CAUTION]
      > In Github, if you leave the page after generating the new token, you will NEVER see it. Thus, copy and paste it into other place (or memorize it if you can).
   3. Paste the new token in GitBash and press `Enter` to continue.
   
7. Then if you see the information which contains a green mark icon, it indicates success.

Such as

```
- gh config set -h github.com git_protocol ssh
✓ Configured git protocol
✓ Logged in as 40843245
```   

Here, a full example of login in GitBash.

```
$ gh auth login
? What account do you want to log into? GitHub.com
? What is your preferred protocol for Git operations on this host? SSH
? Upload your SSH public key to your GitHub account? Skip
? How would you like to authenticate GitHub CLI? Paste an authentication token
Tip: you can generate a Personal Access Token here https://github.com/settings/tokens
The minimum required scopes are 'repo', 'read:org'.
? Paste your authentication token: ****************************************
- gh config set -h github.com git_protocol ssh
✓ Configured git protocol
✓ Logged in as 40843245
```
