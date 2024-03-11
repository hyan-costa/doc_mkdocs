# **POST** Start Valuation

## Rota:
    https://api.prd.valuation.eemovel.com.br/admin/avm-gateway/internal/start_valuation


## Payload:

??? question "Payload"
    * ### **assessing:** *Referente aos dados do IMÓVEL que será avaliado (avaliando)*
        * #### **neighborhood, street, number, city, postal_code, state, complement:**
            * *Bairro, rua, número, Cidade, CEP, Estado e Complemento, respectivamente
            Dados de endereço do avaliando*
        * #### **lat, lon:**
            * *Latitude e Longitude respectivamente, caso não sejam informados, a api vai tentar encontrar através dos dados de endereço do avaliando (pode não ser possível)*
        * #### **area:**
            * *Área total em metros quadrados do avaliando*
        * #### **Category_id:**
            * *Numeração referente ao tipo do imóvel (1 para apartamento e 2 para casa)*
        * #### **sub_category_id:**
             * *Numeração referente ao subtipo do imóvel, se divide em casa e apartamento*
             * *Categorias de casa: 2 (Casa Padrão), 4 (Sobrado), 13 (Casa Geminada), 14 (Casa em Condomínio), 15
                (Sobrado Geminado), 16 (Sobrado em Condomínio);*
             * *Categorias de apartamento: 1 (Apartamento Padrão), 7 (Quitinete), 8 (Studio), 9 (Duplex), 10 (Triplex),
                11 (Flat), 12 (Loft), 22 (Cobertura).*
        * #### **features_bathroom, features_bedroom, features_suite, features_garage:**
            * *Banheiro, quarto, suite e garagem, respectivamente
            Numeração para indicar a quantidade de cada, indo do 1 ao 4*
    * ### **search: :** *referente aos dados que serão usados na busca dos anúncios.* 
        * #### *is_sale:*
            * *true deve ser passado para anúncios de vende e false para aluguel*
        * #### *max_age:*
            * *idade máxima dos anúncios retornados (campo recebido em anos).*
        * #### *neighborhood, street, number, city, postal_code, state, street_long:*
            * *Bairro, rua, número, Cidade, CEP, Estado e Rua (completa sem abreviações), respectivamente
              Dados de endereço da busca*
        * #### **category_id:**
            * *Numeração referente ao tipo do imóvel (1 para apartamento e 2 para casa)*
        * #### **sub_category_id:**
            * *Numeração referente ao subtipo do imóvel, se divide em casa e apartamento*
            * *ategorias de casa: 2 (Casa Padrão), 4 (Sobrado), 13 (Casa Geminada), 14 (Casa em Condomínio),
            15 (Sobrado Geminado), 16 (Sobrado em Condomínio);*
            * *Categorias de apartamento: 1 (Apartamento Padrão), 7 (Quitinete), 8 (Studio), 9 (Duplex), 10 (Triplex),
            11 (Flat), 12 (Loft), 22 (Cobertura).*
            * *Caso não passado será preenchido automaticamente através da subcategoria do avaliando, isso é feito pegando
            todos os outros elementos do grupo escolhido, por exemplo, se no avaliando o número 4 foi informado na busca
            será usado 2, 4, 13, 14, 15, 16, já que os mesmo fazer parte da categoria casa que é o grupo ao qual o 4
            pertence, da mesma forma que se no avaliando o 7 e 11 forem passados na busca será utilizado
            1, 7, 8, 9, 10, 11, 12, 22*
        * #### *area:*
            * *Dividido em área útil (useful) e total (total) recebendo o valor e a porcentagem de margem, onde a margem vai
            ser aplicada no valor da área durante a busca;*
        * #### *price_area:*
            * *Dividido em preço do metro quadrado util (useful) e total (total) dos imóveis, recebendo o valor e a
            porcentagem de margem, onde a margem vai ser aplicada no preço durante a busca;*
        * #### *price_total:*
            * *referente aos preço final dos anúncios, recebe o valor e a porcentagem de margem, onde a margem vai ser
            aplicada no preço durante a busca;*
        * #### *features_bathroom, features_bedroom, features_suite, features_garage:*
            * *Banheiro, quarto, suite e garagem, respectivamente*
            * *Numeração para indicar a quantidade de cada, indo do 1 ao 4*
            * *O 4 é equivalente a ele mesmo e todos os números a cima*
        * #### *radius:*
            * *Raio, caso não informado será automatizado, baseado na densidade de anúncios da região.*
        * #### *lat, lon:* 
            * *Latitude e Longitude respectivamente, caso não sejam informados, a api vai tentar encontrar através dos dados
            de endereço da busca (pode não ser possível)*
        * #### *coordinates:*
            * *Coordenadas, demarcação poligonal que limita a busca a anúncios que estão dentro dessa região delimitada,
            caso não passado a api vai gerar um a partir do raio juntamente com a latitude e longitude*
    * ### **more_filters:** *filtros aplicados na busca das amostras/anuncios*
        * #### *remove_duplicates:*
            * *Remove anúncios duplicados;* 
        * #### *full_address:*
            * *Apenas anúncios com endereço completo.*
        * #### *active_ads:*
            * *Retorna apenas anúncios ativos.*
            * *Esse filtro faz uma predição considerando as datas de atualização do anúncio mas, não é possivel prever com 
            exatidão pois, isso está hospedado em um portal terceiro e sujeito a variação.*
        * #### *recent_ads:*
            * *Apenas anuncios recentes*
        * #### *min_quantity_ad:*
            * *Define a quantidade mínima de anúncios que serão selecionados.*
        * #### *min_similarity:*
            * *Quantidade minima de similaridade que o anúncio encontrado deve ter para ser
            considerado (recebe um valor entre 0 e 1).*



## Request:
??? question  "Example Request"
    * *method: GET*

    === "Request"
            curl --location 'https://api.prd.valuation.eemovel.com.br/admin/avm-gateway/internal/start_valuation' --header 'x-api-key: apikey' --data 'json'
    
    === "Body"
        **json:**
        ```{ .json .select}
            {
              "search": {
                "is_sale": true,
                "max_age": 0,
                "address": {
                  "street": "R. Iguatinga",
                  "neighborhood": "Santo Amaro",
                  "city": "São Paulo",
                  "postal_code": "04744-040",
                  "state": "SP",
                  "street_long": "Rua Iguatinga"
                },
                "realty_type": {
                  "category_id": [
                    1, 2
                  ],
                  "sub_category_id": [
                    1, 2
                  ]
                },
                "area": {
                  "useful": {
                    "value": 45,
                    "percentage": 40
                  },
                  "total": {
                    "value": 0,
                    "percentage": 100
                  }
                },
                "price_area": {
                  "useful": {
                    "value": 0,
                    "percentage": 100
                  },
                  "total": {
                    "value": 0,
                    "percentage": 100
                  }
                },
                "price_total": {
                  "value": 0,
                  "percentage": 100
                },
                "typology": {
                  "features_bathroom": [],
                  "features_bedroom": [],
                  "features_suite": [],
                  "features_garage": []
                },
                "location": {
                  "radius": 1500,
                  "lat": -23.6571986,
                  "lon": -46.7045881
                }
              },
              "assessing": {
                "category_id": 1,
                "lat": -23.6571986,
                "lon": -46.7045881,
                "neighborhood": "Santo Amaro",
                "area": 45,
                "street": "R. Iguatinga",
                "sub_category_id": 1,
                "city": "São Paulo",
                "postal_code": "04744-040",
                "state": "SP",
                "complement": "apto 1202, bloco C",
                "typology": {
                  "features_bathroom": 1,
                  "features_bedroom": 1,
                  "features_suite": 1,
                  "features_garage": 1
                }
              },
              "more_filters": {
                "full_address": true,
                "remove_duplicates": true,
                "active_ads": true,
                "recent_ads": false,
                "min_quantity_ad": 2
              }
            }
        ```
    === "Headers (13)"
             x-api-key                               your_api_key



## Response:
??? question  "Example Response"

    === "Body"

        ``` { .json .select}
        {
          "data": "b48387c642ec45c0b0e007b96f3076bd",
          "message": "Busca de anúncios iniciada com sucesso!",
          "code": 200,
          "success": true
        }
        ```

    === "Headers (13)"

        
            Content-Type                            application/json

            Content-Length                          134

            Connection                              keep-alive

            Date                                    Wed, 29 Nov 2023 23:42:46 GMT

            x-amzn-RequestId                        00c6df2a-6f4a-4412-988e-9c7f83ee71db

            Access-Control-Allow-Origin             *

            x-amzn-Remapped-Content-Length          134

            x-amz-apigw-id                          PLzgTEJIIAMEdEQ=

            X-Amzn-Trace-Id                         Root=1-6567cc68-73b8c97e28dd95ee4eda0e53

            X-Cache                                 Miss from cloudfront

            Via                                     1.1 39c56f5335aa583fff94230bb4959d02.cloudfront.net (CloudFront)

            X-Amz-Cf-Pop                            FOR50-P3

            X-Amz-Cf-Id                             gYljOHAGDjgHiww38_7Mlo6xveeG4UutYqf87-ESs2oedKpVh6JXUA==
    
