# Tarefa Resource

Esta API permite o controle total das tarefa. Veja as instruções de como realizar a integração abaixo.

Instruções para realizar a integração:

URL
http://app.nectarcrm.com.br/crm/api/1/tarefas/

[Para mais informações, consulte a documentação completa clicando aqui](http://docs.nectarcrm.apiary.io)

Schema Info | [Schema JSON](schema.json)

Propriedade | Tipo | Descricao
------------ | ------------- | -------------
autor | (object) | Autor do contato
autorAtualizacao | (object) | Quem fez a última atualização
cliente | (object) | Contato relacionado a venda
dataAtualizacao | (datetime) | Última data de atualização
dataCriacao | (datetime) | Data de criação desse contato
dataLimite | (datetime) | Data limite para realizar a tarefa
descricao | (string) | Descrição do tarefa
id | (long) | Identificador no sistema
prioridade | (integer) | Prioridade da tarefa (0 = Normal, 1 = Alta, 2 = Altíssima)
responsavel | (object) | Quem será responsável por esse contato
status | (integer) | Status da tarefa (0 = Aberta, 1 = Concluída, 2 = Cancelada, 3 = Em execução)
tipo | (object){"id", "nome"} | Tipo do tarefa (cadastrado, se não existir iremos incluir)
titulo | (string) | Titulo da tarefa

Exemplo
```js
    {
        "cliente": {
          "id": 430,
          "nome": "Colmeia Soluções"
        },
        "dataLimite": 1455391629560,
        "descricao": "Tarefa tese descrição",
        "prioridade": 2,
        "responsavel": {
          "id": 12,
          "login": "usuario1",
          "nome": "Usuario 1"
        },
        "status": 0, //aberta
        "tipo": "Reunião",
        "titulo": "Teste de tarefa"
      }
```