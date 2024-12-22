# Upload de Arquivos e Detecção de Cartão de Crédito com Azure

Este projeto permite o upload de imagens para o Azure Blob Storage, onde são processadas para detectar informações de cartões de crédito, utilizando o **Azure Document Intelligence**. A interface é construída com **Streamlit** para facilitar a interação com o usuário.

## Funcionalidades

- **Upload de Imagens**: Permite o upload de arquivos de imagem (formatos: PNG, JPG, JPEG) para o Azure Blob Storage.
- **Análise de Cartão de Crédito**: Utiliza o Azure Document Intelligence para extrair informações como nome do titular, número do cartão, banco emissor e data de validade.
- **Interface Intuitiva**: Exibe a imagem carregada e apresenta os resultados da análise indicando se o cartão é válido.

## Requisitos do Azure

Para rodar o projeto, é necessário configurar os seguintes serviços no Azure:

- **Conta de Armazenamento e Contêiner**: Usado para armazenamento das imagens carregadas.
- **Azure Document Intelligence**: Utilizado para a detecção e extração de informações de cartões de crédito nas imagens.



## Como Utilizar

### 1. Clone o Repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd <NOME_DO_REPOSITORIO>

### 2. Renomear o .env copy para ".env" e preencher os dados

## Onde obter os dados:

- CONTAINER_NAME
![CONTAINER_NAME](src/img/CONTAINER_NAME.png)
- AZURE_STOREGE_CONNECTION_STRING: 
![AZURE_STOREGE_CONNECTION_STRING](src/img/AZURE_STOREGE_CONNECTION_STRING.png)
- ENDPOINT: 
![ENDPOINT](src/img/ENDPOINT.png)
- SUBSCRIPTION-KEY: 
![SUBSCRIPTION-KEY](src/img/SUBSCRIPTION-KEY.png)


## Permissões necessárias:

- A conta de armazenamento deve ter "acesso anonimo ao blob" habilitado
![permissaoBlob](src/img/permissaoBlob.png)

- Container deve estar com o nivel de acesso "Container (anonimo)"
![permissaoBlob](src/img/permissaoBlob1.png)

### 3. Adicionar os requirements

- pip install -r requirements.txt

### 4. Rodar o programa

- Abrir no terminal a pasta src e utilizar `streamlit run .\app.py`


