# API Generated

## Descrição
{"documentation": "# Documenta\u00e7\u00e3o da API FastAPI\n\nEsta API em FastAPI gerencia eventos. Os eventos s\u00e3o representados por um nome, data e localiza\u00e7\u00e3o.\n\n## Endpoints\n\n### Criar Evento\n- **M\u00e9todo:** POST\n- **URL:** /events/\n- **Par\u00e2metros:**\n    - event (corpo da requisi\u00e7\u00e3o): Evento a ser criado\n        - name (str): Nome do evento\n        - date (str): Data do evento\n        - location (str): Localiza\u00e7\u00e3o do evento\n- **Retorno:** Retorna o evento criado\n- **Exemplo de uso:**\n    ```bash\n    curl -X POST \"http://localhost:8000/events/\" -H \"Content-Type: application/json\" -d '{\"name\": \"Anivers\u00e1rio\", \"date\": \"2023-08-15\", \"location\": \"Casa\"}'\n    ```\n\n### Obter Todos os Eventos\n- **M\u00e9todo:** GET\n- **URL:** /events/\n- **Retorno:** Retorna uma lista de todos os eventos cadastrados\n- **Exemplo de uso:**\n    ```bash\n    curl -X GET \"http://localhost:8000/events/\"\n    ```\n\n### Obter Evento por ID\n- **M\u00e9todo:** GET\n- **URL:** /events/{event_id}\n- **Par\u00e2metros:**\n    - event_id (int): ID do evento a ser obtido\n- **Retorno:** Retorna o evento correspondente ao ID informado\n- **Exemplo de uso:**\n    ```bash\n    curl -X GET \"http://localhost:8000/events/0\"\n    ```\n\n### Atualizar Evento por ID\n- **M\u00e9todo:** PUT\n- **URL:** /events/{event_id}\n- **Par\u00e2metros:**\n    - event_id (int): ID do evento a ser atualizado\n    - event (corpo da requisi\u00e7\u00e3o): Dados atualizados do evento\n        - name (str): Nome do evento\n        - date (str): Data do evento\n        - location (str): Localiza\u00e7\u00e3o do evento\n- **Retorno:** Retorna o evento atualizado\n- **Exemplo de uso:**\n    ```bash\n    curl -X PUT \"http://localhost:8000/events/0\" -H \"Content-Type: application/json\" -d '{\"name\": \"Anivers\u00e1rio Modificado\", \"date\": \"2023-08-15\", \"location\": \"Sal\u00e3o de Festas\"}'\n    ```\n\n### Deletar Evento por ID\n- **M\u00e9todo:** DELETE\n- **URL:** /events/{event_id}\n- **Par\u00e2metros:**\n    - event_id (int): ID do evento a ser deletado\n- **Retorno:** Retorna o evento deletado\n- **Exemplo de uso:**\n    ```bash\n    curl -X DELETE \"http://localhost:8000/events/0\"\n    ```\n\n## Notas Importantes\n- Os eventos s\u00e3o armazenados em mem\u00f3ria, ou seja, n\u00e3o s\u00e3o persistentes entre reinicializa\u00e7\u00f5es do servidor.\n- Os IDs dos eventos s\u00e3o baseados na ordem em que foram criados, come\u00e7ando em 0.\n- Em caso de erro ao acessar um evento por ID (por exemplo, ID inv\u00e1lido), ser\u00e1 retornado um erro 404 (Not Found).\n\n## Depend\u00eancias Necess\u00e1rias\n- FastAPI\n- Pydantic\n- typing"}

## Instalação
1. Clone o repositório
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

## Uso
Execute o servidor:
```bash
uvicorn src.main:app --reload
```

## Documentação
Consulte a pasta `docs` para a documentação completa do projeto.
