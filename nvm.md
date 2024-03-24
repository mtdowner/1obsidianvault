To **install** or **update** nvm, you should run the [install script](https://github.com/nvm-sh/nvm/blob/v0.39.7/install.sh). To do that, you may either download and run the script manually, or use the following cURL or Wget command:

```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

```shell
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
```

Running either of the above commands downloads a script and runs it. The script clones the nvm repository to `~/.nvm`, and attempts to add the source lines from the snippet below to the correct profile file (`~/.bash_profile`, `~/.zshrc`, `~/.profile`, or `~/.bashrc`).

```shell
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

[#### [Additional Note](https://github.com/nvm-sh/nvm?tab=readme-ov-file#additional-notes)

- If the environment variable `$XDG_CONFIG_HOME` is present, it will place the `nvm` files there.
    
- You can add `--no-use` to the end of the above script (...`nvm.sh --no-use`) to postpone using `nvm` until you manually [`use`](https://github.com/nvm-sh/nvm?tab=readme-ov-file#usage) it.
    
- You can customize the install source, directory, profile, and version using the `NVM_SOURCE`, `NVM_DIR`, `PROFILE`, and `NODE_VERSION` variables. Eg: `curl ... | NVM_DIR="path/to/nvm"`. Ensure that the `NVM_DIR` does not contain a trailing slash.
    
- The installer can use `git`, `curl`, or `wget` to download `nvm`, whichever is available.
    
- You can instruct the installer to not edit your shell config (for example if you already get completions via a [zsh nvm plugin](https://github.com/ohmyzsh/ohmyzsh/tree/master/plugins/nvm)) by setting `PROFILE=/dev/null` before running the `install.sh` script. Here's an example one-line command to do that: `PROFILE=/dev/null bash -c 'curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash'`