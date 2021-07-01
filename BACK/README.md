
# AutoVap - Back-end
Bem vindo ao back-end do projeto AutoVap, aqui se encontra toda a API responsável pela parte app e web da aplicação.
- Tenha certeza de ter seguido os passos do readme que se encontra na [raiz](https://github.com/DaniloServulo/unibh-apresentacao/blob/main/README.md) do nosso github

## Rodando o projeto
### Configurando o ambiente
- Abra o terminal do seu OS e navegue até a pasta responsável por esta parte da aplicação(`BACK/autovap_api`)
- Execute o seguinte comando
```
npm install --from-lock-file
```

### Configurando a base de dados
- Certifique-se que o [XAMPP](https://www.apachefriends.org/pt_br/download.html)(para qualquer OS), [WampServer](https://www.wampserver.com/en/)(para Windows), [MAMP](https://www.mamp.info/en/downloads/)(para Mac) ou [LAMP](https://www.techtudo.com.br/dicas-e-tutoriais/noticia/2012/11/como-instalar-lamp-no-linux.html)(para Linux) está instalado
- Através de um destes mencionados acima acesse o phpmyadmin e crie um banco de dados para a aplicação
- Certifique-se de que seu usuário possui as permissões necessárias para executar operações no banco de dados, em caso de dúvida sobre como fazer isto você pode consultar este [link](https://www.youtube.com/watch?v=MBF02LurEHg)
- Abra seu projeto e navegue até o arquivo datastores.js(`BACK/autovap_api/config/datastores.js`)
- Execute o comando abaixo
```
npm install sails-mysql --save
```
- Altere as credenciais de acordo com seu banco de dados local
- `ORIGINAL`
```
url: 'mysql://db_user:db_password@host:port/db_name'
```
- `EXEMPLO`
```
url: 'mysql://root:autovap@localhost:3306/autovap_db'
```
- Navegue até o arquivo models.js(`BACK/autovap_api/config/models.js`)
- Na seguinte linha de código alterar de `safe` para `alter`
- `ORIGINAL`
```
migrate: 'safe'
```
- `ALTERADO`
```
migrate: 'alter'
```

### Executando o projeto
- O projeto foi feito utilizando o Sails (versão `1`)
- Execute o seguinte comando dentro da pasta BACK/autovap_api no seu terminal
```
sails lift
```
