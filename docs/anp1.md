Análise de Tráfego HTTP

1. Primeira Requisição (MDN Web Docs)
    Método: GET  URL: https://developer.mozilla.org/  
    Status: 200 OK  

2. Recursos Estáticos
    Arquivo CSS:
        URL: https://developer.mozilla.org/static/client/styles-global.13616ebb1fc8ee2f.css  
        Status: 200 OK  
        Content-Type: text/cssArquivo 
        
    JavaScript:
        URL: https://developer.mozilla.org/static/client/8839.d36534ceeb519909.js  
        Status: 200 OK  
        Content-Type: application/javascript
        
    Imagem (SVG):
        URL: https://developer.mozilla.org/static/ssr/languages.dcba936080e5be86.svg  
        Status: 200 OK  
        Content-Type: image/svg+xml
        
3. Simulando um Erro 404
    Ao editar a URL para um caminho que não existe, a resposta é diferente de um 200 OK. O código de status muda para 404 Not Found. 
    A principal diferença observada na resposta é que o servidor, em vez de enviar o conteúdo do site, retorna uma página de erro em HTML informando que o recurso não foi encontrado.  
    
4. Requisição de API (Busca do YouTube)
    Método: 
        GET  Caminho (URL da requisição de busca): [https://suggestqueries-clients6.youtube.com/complete/search?ds=yt&hl=pt&gl=br&client=youtube&gs_ri=youtube&tok=-G6HCsQyfVqhY55r7i_6TQ&h=180&w=320&ytvs=1&gs_id=c&q=corinthians&cp=11&pq=corinthians]
        Status: 200 OK  
        Comparação: Assim como visto nesta requisição real do YouTube, a nossa tabela ação x método x rota no arquivo docs/requisitos.md também utiliza o método GET para operações de leitura e busca. Em ambos os casos, a URL e seus parâmetros definem o que está sendo buscado.
        
5. Rota para o Cine TrackPara listar os filmes no projeto Cine Track, usaremos o método GET na rota /filmes. 
    Essa definição é coerente com a arquitetura REST, onde a URL identifica claramente o recurso a ser acessado (os filmes) e o método expressa a operação desejada (buscar/ler). No corpo da resposta a essa requisição, o servidor deverá retornar a lista de filmes, estruturada no formato JSON.  
