# Instalação e configuração das ferramentas de desenvolvimento

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

## Configuração do oh-my-zsh (OPCIONAL)
- Para auxiliar no desenvolvimento utilizamos o oh-my-shell um framework para o zsh que auxilia com autocomplete e syntax-highlighting

Para instalar o oh-my-zsh utilize o seguinte comando:
```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Agora baixe os plugins:
- Autosuggestions:
```shell
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions
```

- Syntax-Highlighting 
```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
```

- Abra o arquivo de shell:
```shell
code ~/.zshrc
```

na linha de plugins do .zshrc cole as seguintes linhas:




## Instalando o NVM
Instale o [nvm](https://github.com/nvm-sh/nvm "https://github.com/nvm-sh/nvm") para gerênciamento das versões do node.

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

### Agora é necessário adiciona-la ao PATH do seu sistema operacional, para isso, adicione o seguinte código:

**Abra o arquivo do seu shell com o seguinte comando:**

- Para abrir no VS Code:  
  ```shell
  code ~/.zshrc


- Para abrir com o nano:  
  ```shell
  nano ~/.zshrc

- Para abrir com o vim:  
  ```shell
  vim ~/.zshrc

| Ao final do seu arquivo (`.zshrc` ou `.bash_profile` ou `.bashrc`) cole a seguinte linha:

```shell
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```


Após isso utilize o comando abaixo para dar refresh no PATH.

```shell 
source ~/.zshrc
```

Para verificar sua instalação use comando:

```shell
nvm -v
```

Instale o [node](https://nodejs.org "https://nodejs.org/") versão `16.16.0` com a nvm.

```shell
nvm install 16.16.0 && nvm use 16.16.0 && node -v
```


## Instalando o yarn
Instale o [yarn](https://classic.yarnpkg.com "https://classic.yarnpkg.com/") globalmente

```shell
npm install --global yarn
```

## Instale o [RVM](https://rvm.io/ "https://rvm.io/") para gerenciar as versões do ruby

```shell
brew install gnupggpg --keyserver hkp://keys.gnupg.net    --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3\curl -sSL https://get.rvm.io | bash -s stable --ruby
```

Agora instale a versão `2.7.6` do ruby que é a requerida pelo projeto

```
rvm install 2.7.6rvm use 2.7.6
```

## Instalação do watchman

Instale o [watchman](https://facebook.github.io/watchman/"https://facebook.github.io/watchman/")

```shell
brew updatebrew install watchman
```

## Instalação da JDK(Java Development Kit) 

- Instale o sdkman para gerenciar as versões da JDK com o seguinte comando:

```shell
curl -s "https://get.sdkman.io" | bash
```

- Depois execute o seguinte comando:

```shell
source "$HOME/.sdkman/bin/sdkman-init.sh"
```

- Instale a JDK 17 com o seguinte comando:

```shell
sdk install java 17.0.12-amzn
```

- Ele vai te perguntar se deseja setar a versão 17 como default dê y para sim


## Configuração das variáveis de ambiente ANDROID_HOME e JAVA_HOME

- Em seu arquivo de shell:
```shell
code ~/.zshrc
```

Cole as seguintes linhas nele:
```shell
# JAVA_HOME
export JAVA_HOME="$HOME/.sdkman/candidates/java/current"
```

```shell
# ANDROID_HOME CONFIG
export ANDROID_HOME=~/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/platform-tools
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
```

## Instalação do Flipper
- Faça o download do flipper no seguinte link [Flipper](https://fbflipper.com/)
  - O flipper é como se fosse um chrome dev tools, nos ajuda a achar logs e ver as requisições do App