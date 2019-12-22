# `nvm` (Node Version Manager)

[nvm (GitHub)](https://github.com/nvm-sh/nvm)

Bash script, not binary executable, so use command -v nvm to verify; won’t show up with which nvm.

## Install

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | zsh
```

Check GitHub repo for latest version. Replace `zsh` with `bash` if using bash.

Script clones nvm repo to `~/.nvm` and adds source line to profile (`~/.bash_profile`, `~/.bashrc`, or `~/.zshrc`).

```sh
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```

## Usage

### Install current release line

```script
nvm install node # "node" is alias for latest version
```

### Install latest active LTS

```sh
nvm install --lts
```

Or specific LTS:

```sh
nvm install lts/carbon
```

### Install specific version

```sh
nvm install 6.14.4
```

### List all available versions

```sh
nvm ls-remote
```

### List local versions

```sh
nvm ls
```

### Install latest npm

```sh
nvm install --latest-npm
```

### Use particular version

```sh
nvm use node|default|system|--lts|<version number>
```

`default` points to first version installed (use `nvm alias default <version>` to change).

Similarly, `nvm run`, `nvm exec`.

```sh
nvm run 8.15.1 app.js
nvm exec 10.13.0 node app.js # run `node app.js` in subshell with PATH pointing to node 10.13.0
```

### Uninstall

```sh
nvm uninstall 10.17.0
```

## .nvmrc

Can create `.nvmrc` containing node version number (or any other string that nvm understands) in project root directory (or any parent directory). Afterward, `nvm use`, `nvm install`, `nvm exec`, `nvm run`, and `nvm which` will use this version if no version supplied on command line.

```sh
echo "lts/*" > .nvmrc # to default to latest LTS version
```

Must contain only version. No trailing space, must have trailing newline.
