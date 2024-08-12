
## Install

To run this git server a number of files and directories are required. A skeleton set of directories and files are made available in this git repo. Above all, do not include sensitive data (ie secrets, usernames, etc.) in any sort of version control. 

### Untrack Staged Changes

If edits you've made are included by git as untracked changes, a command you can use to remove that file from tracked changes is emulated below. In this example, the tailscale auth key file is untracked after manually updating the auth key from a password vault. 

```sh 
git update-index --assume-unchanged .\secrets\ts_authkey.txt
```

### Secrets to Include Locally

<div class="tg-wrap"><table><tbody>
  <tr>
    <th>Variable</td>
    <th>Filename</td>
    <th>Description</td>
    <th>More Reading</td>
  </tr>
  <tr>
    <td><code>TS_AUTHKEY</code></td>
    <td>ts_authkey.txt</td>
    <td>tail scale auth key</td>
    <td><a href="https://login.tailscale.com/admin/settings/keys" target="_blank" rel="noopener noreferrer">Generate new Auth Key</a></td>
  </tr>
  <tr>
    <td><code>SOFT_SERVE_INITIAL_ADMIN_KEYS</code></td>
    <td>initial_admin_keys.txt</td>
    <td>public key used to authenticate against git server</td>
    <td><a href="https://github.com/charmbracelet/soft-serve" target="_blank" rel="noopener noreferrer">Repo home page</a><br></td>
  </tr>
</tbody>
</table></div>
