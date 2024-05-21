# Extração de Comentários do YouTube

Este Jupyter Notebook permite extrair comentários e respostas de vídeos do YouTube usando a YouTube Data API v3. Ele exporta os dados para um arquivo CSV.

## Pré-requisitos

Para executar este notebook, você precisa:
- Ter uma chave de API do Google Cloud habilitada para acessar a YouTube Data API v3.
- Conhecer o ID do vídeo do YouTube do qual deseja extrair os comentários.

## Configuração

1. Substitua `YOUR_API_KEY` pela sua chave de API do Google Cloud.
2. Substitua `VIDEO_ID` pelo ID do vídeo do qual deseja extrair os comentários.

## Como Executar

Execute cada célula do notebook sequencialmente:
1. Importe as bibliotecas necessárias e configure a API.
2. Execute a função `get_comment_threads` para coletar os comentários e as respostas, e exporte os resultados para um arquivo CSV chamado `youtube_comments_with_replies.csv`.

## Arquivo de Saída

O arquivo `youtube_comments_with_replies.csv` contém as seguintes colunas:
- `author`: Nome do autor do comentário ou resposta.
- `message`: Texto do comentário ou resposta.
- `date`: Data de publicação do comentário ou resposta.
- `reply_to`: Nome do autor do comentário original a que a resposta se destina, se aplicável.

### Nota

Este script está limitado a extrair até 100 comentários e respostas por requisição à API, conforme o limite imposto pela API do YouTube. Mas faz mais de uma requisição com o nextpage token. 

