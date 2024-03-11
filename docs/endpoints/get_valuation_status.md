# **GET** Valuation Status


## Rota:
    https://api.prd.valuation.eemovel.com.br/admin/avm-gateway/internal/get_valuation_status/54e919851bb94c32b00670dc53751022

Nesta rota é possível ter acesso ao progresso em que a avaliação se encontra:

* Search: onde de fato ocorre a busca pelas amostras;
* Selection: são selecionadas as amostras baseadas nos índices de similaridade com o avaliando;
* Price: após a seleção é realizado um conjunto de cálculos para obter o valor final do imóvel avali

Após a precificação final do imóvel é calculado também o seu limite inferior e superior.


Quando todos os passos estiverem completos é possível acessar e baixar o Laudo Final através do link:
    ``` url
        https://avm.eemovel.com.br/laudo/3e7073fbeb654b89af1a87a3f17e5205
    ```


## Request:
??? question  "Example Request"
    * *method: GET*
    === "Request"
            curl --location 'https://api.prd.valuation.eemovel.com.br/admin/avm-gateway/internal/get_valuation_status/b48387c642ec45c0b0e007b96f3076bd' --header 'x-api-key: apikey'
    === "Headers (1)"
             x-api-key                               your_api_key

## Response:
??? question "Example Response"

    === "Body"
        ``` { .json .select }
        {
          "data": {
            "price": 387283.34,
            "lower_limit": 348555.00600000005,
            "upper_limit": 426011.67400000006,
            "progress": {
              "selection": true,
              "search": true,
              "price": true
            },
            "created_at": "2023-11-29T23:42:45.874757Z",
            "updated_at": "2023-11-29T23:42:56.599499Z",
            "error_message": null
          },
          "message": "Avaliação encontrada com sucesso!",
          "code": 200,
          "success": true
        }
        ```
    
    === "Headers(13)"
            Content-Type                            application/json
    
            Content-Length                          6899
    
            Connection                              keep-alive
    
            Date                                    Wed, 29 Nov 2023 23:45:11 GMT
    
            x-amzn-Request                          Id866b8b8b-2b3c-4820-bf53-91c30ffaf47e
    
            Access-Control-Allow-Origin             *

            x-amzn-Remapped-Content-Length          6899

            x-amz-apigw-id                          PLz4nFHvoAMEd8g=

            X-Amzn-Trace-Id                         Root=1-6567cd03-3af007f02ec660411991ea13

            X-Cache                                 Miss from cloudfront

            Via                                     1.1 39c56f5335aa583fff94230bb4959d02.cloudfront.net (CloudFront)

            X-Amz-Cf-Pop                            FOR50-P3

            X-Amz-Cf-Id                             3qbEWJKxXD8ycEs_GHMaQHnfGg5wlSMsoaKsy98_WhkdwFG1MuzbKA==
           
