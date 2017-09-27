# apidoc

#### Como ler e escrever este documento

```
#ENDPOINT -> Rota da api
@Model -> modelo( estrutura ) de dados desse endpoint
>> -> Corpo da requisição
: -> Descrição do funcionamento
<< -> Retorno de requisição
/ -> Endereço ( sub-rotas )
! -> Tipo de requisição GET, POST
(#) -> Cabeçalhos ?
```

### Exemplo de uso na escrita

Exemplo de adição
```
#Empresa
/empresas
!POST (application/json)
>> @Empresa
: Salva empresa no banco de dados e recupera sua chave primária.
<< id:10
```

Exemplo de leitura
```
#Empresa
/empresas
!GET (application/json)
: Recupera do banco de dados.
<< @Empresas[]
```
