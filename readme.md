# Relatório Automatizado

Este script Python automatiza o processo de obtenção, processamento e armazenamento de relatórios de atendimento de uma API. Ele realiza as seguintes etapas

## Estrutura de Arquivos

1. **Acesso à API:** Obtém um token de acesso para autenticar a conexão com a API.
2. **Cálculo de Datas:** Calcula os parâmetros de data de início e fim para os relatórios.
3. **Obtenção de Dados:** Faz uma solicitação à API para obter os dados de atendimento dentro do intervalo de datas especificado.
4. **Processamento de Resposta:** Verifica se a solicitação foi bem-sucedida e, em caso afirmativo, salva os dados em um arquivo local no formato .xls.
5. **Modificação do Arquivo:** Remove informações desnecessárias do arquivo .xls.
6. **Inserção de Dados:** Insere os dados processados no banco de dados.
7. **Limpeza:** Remove o arquivo temporário gerado durante o processo.

## Como Usar

1. **Instalação de Dependências**: Certifique-se de ter as bibliotecas necessárias instaladas. Você pode instalá-las executando o seguinte comando:

   ```bash
   pip install pandas sqlalchemy requests
   ```
2. **Configuração** : Abra o arquivo `config.py` e insira suas credenciais de API e do banco de dados.
3. **Execução do Script** : Execute o script `main.py` para iniciar o processo automatizado. O script realizará as seguintes etapas:

* Obter o token de acesso da API.
* Calcular o intervalo de datas para a requisição à API.
* Realizar a requisição à API para obter os dados de atendimento.
* Salvar os dados em uma planilha Excel local chamada `output.xls`.
* Processar a planilha, realizando ajustes e removendo informações desnecessárias.
* Inserir os dados processados no banco de dados.

4. **Limpeza** : O script também apaga a planilha temporária `output.xls` após o processamento.

## Observações Importantes

* Para utilizar este script, é necessário ter acesso à API de relatórios de atendimento, bem como as bibliotecas `api_requests`, `date_handler`, `spreadsheet_handler`, e `database` devem estar disponíveis no ambiente Python.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir problemas ou enviar solicitações de pull para melhorar este projeto.
