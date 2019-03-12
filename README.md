# Installing Pyenv
Step-by-step

1. `brew install pyenv` 
1. Define environment variable: In terminal, enter `nano ~/.bash_profile` and then paste the following, then save and exit: 
`$ echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile` followed by,
`$ echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile`
1. Add `pyenv init` to shell via the following command:
`$ echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile`
1. Restart shell via `exec "$SHELL"`
1. Install `pyenv-virtualenv` via `brew install pyenv-virtualenv`
1. Add the following in Terminal:
`eval "$(pyenv init -)"` 
and 
`eval "$(pyenv virtualenv-init -)"`
1. For Mojave: Install `zlib` via `brew install zlib`
1. Add the following to ~/.zshrc (Use command `nano ~/.zshrc`):
`# For compilers to find zlib you may need to set:
export LDFLAGS="${LDFLAGS} -L/usr/local/opt/zlib/lib"
export CPPFLAGS="${CPPFLAGS} -I/usr/local/opt/zlib/include"`
`# For pkg-config to find zlib you may need to set:
export PKG_CONFIG_PATH="${PKG_CONFIG_PATH} /usr/local/opt/zlib/lib/pkgconfig" `
1. Create a new Virtual Environment with `pyenv install 3.x.x`
2. `pyenv virtualenv 3.x.x name_of_env`
3. `pyenv activate name_of_env`

