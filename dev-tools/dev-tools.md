# Instalação das ferramentas de desenvolvimento


## Instalando o Homebrew
Instale o [Homebrew](https://brew.sh "https://brew.sh/") para gerenciamento de pacotes.

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Caso seu CHIP seja `M1,M2` adicione a seguinte linha no seu arquivo (`.zshrc` ou `.bash_profile` ou `.bashrc`)

```
export PATH="/opt/homebrew/bin:/opt/homebrew/sbin${PATH+:$PATH}";
```

## Instalando o git
Instale o [git](https://git-scm.com "https://git-scm.com/").

```
brew install git
```

## Instalando o NVM
Instale o [nvm](https://github.com/nvm-sh/nvm "https://github.com/nvm-sh/nvm") para gerênciamento das versões do node.

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

### Agora é necessário adiciona-la ao PATH do seu sistema operacional, para isso, adicione o seguinte código:

```
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

ao final do seu arquivo de PATH code (`.zshrc` ou `.bash_profile` ou `.bashrc`), que pode ser acessado com os comandos:

- ```shell
code  ~/.zshrc
```
- ```shell
nano  ~/.zshrc
```- ```shell
vim  ~/.zshrc
```


Após isso utilize o comando abaixo para dar refresh no PATH.

```
source ~/.zshrc
```

Para verificar sua instalação use comando:

```
nvm -v
```

Instale o [node](https://nodejs.org "https://nodejs.org/") versão `16.16.0` com a nvm.

```
nvm install 16.16.0nvm use 16.16.0node -v
```

Instale o [yarn](https://classic.yarnpkg.com "https://classic.yarnpkg.com/") globalmente

```
npm install --global yarn
```

Instale a [RVM](https://rvm.io/ "https://rvm.io/") para gerenciar as versões do ruby

```
brew install gnupggpg --keyserver hkp://keys.gnupg.net    --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3\curl -sSL https://get.rvm.io | bash -s stable --ruby
```

Agora instale a versão `2.7.6` do ruby que é a requerida pelo projeto

```
rvm install 2.7.6rvm use 2.7.6
```

Instale o [watchman](https://facebook.github.io/watchman/ "https://facebook.github.io/watchman/")

```
brew updatebrew install watchman
```

