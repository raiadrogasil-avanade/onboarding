# Rodando o aplicativo no android

- Na pasta dos seu aplicativo rode o seguinte comando para instalar as dependências:
```shell
yarn
```

- Dê cd dentro de app e rode novamente yarn:
```shell
yarn
```

- Após isso dê cd .. para voltar para raiz e rode o seguinte comando:
```shell
yarn android:raia:dev
```
| Para rodar em drogasil basta trocar o raia por ```sil```

O comando é composto pelas seguintes partes:

- ```android``` plataforma na qual estamos rodando
- ```raia``` a bandeira que vamos utilizar 
-  ```dev``` o ambiente que queremos utilizar(dev,stg,prod)

# Rodar o app em IOS
- Para rodar o app em ios segue um outro readme explicando: [Rodar app em IOS](https://gitlab.com/gsmalheiro.avanade/readme-rodar-ios)