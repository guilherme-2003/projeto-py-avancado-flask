# projeto-py-avancado-flask

O projeto é uma ferramenta de WebScraper (Ferramenta para coletar dados de uma página web), ele coleta as partes fundamentais da notícia e as divide da seguinte forma:

"Notícia X": {
        "Tittle": "Título da matéria",
        "Notice": "Link da notícia oficial",
        "Image": "Src da imagem (Link do local web onde a imagem da matéria está)",
        "Date": "Quanto tempo faz que a notícia foi postada"

Essas informações vem do portal de notícias https://g1.globo.com através de um método POST. Através do POSTMAN é possível enviar uma informação que precisa ser em formato JSON e na seguinte configuração:

{
    "Escolhas": ["Tema"]
}

Primeiro deve substituir o "Tema" por UM ou VÁRIOS temas separados por vírgula. Aqui está uma lista de temas disponíveis e um exemplo de como eles precisam ser organizados:

agro, ciencia, economia, educacao, eleicoes, empreendedorismo, fato-ou-fake, inovacao, mundo, politica.

Todos os itens acima são elegíveis para serem passados como parâmetros de "Escolhas", precisam ser organizados seguindo o exemplo:

{
    "Escolhas": ["politica", "economia", "ciencia"]
}

Antes de enviar essa requisição pelo Postman é preciso executar o arquivo scraper.py

Ele constará que está em execução no terminal. 

Após esse passo, é possível navegar até o postman e selecionar o metódo POST, adicionar o link: http://localhost:5000/noticias, selecionar a aba Body>raw e tipo JSON.

Assim será possível enviar quais as notícias que você deseja ver. 

Você receberá um status 200 como confirmação, ao navegar na pasta webscrapping/templates notará um arquivo criado e chamado de Notícias.json

Nele estaram constadas todas as 10 notícias mais recentes de cada tema escolhido. Ou seja, irá resultar em um arquivo json contendo título, link da notícia, link da imagem da matéria e há quanto tempo ela foi ao ar.

O objetivo do projeto é conseguir criar um portal de notícias que relacione notícias curtas e atuais de diversos temas e portais diferentes.
