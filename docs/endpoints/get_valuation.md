# **GET** Valuation


## Rota:
    https://api.prd.valuation.eemovel.com.br/admin/avm-gateway/internal/get_valuation/54e919851bb94c32b00670dc53751022

Esta rota traz todos os dados referente à avaliação:

* Endereços inputados no inicio da avaliaçao (rota /start_valuation);
* Anúncios selecionados com base na filtragem;
* Valores referentes a precificaçao final da avaliaçao.



## Request:
??? question  "Example Request"
    * *method: GET*
    === "Request"
            curl --location 'https://api.prd.valuation.eemovel.com.br/admin/avm-gateway/internal/get_valuation/b48387c642ec45c0b0e007b96f3076bd' --header 'x-api-key: apikey'
    === "Headers (1)"
             x-api-key                               your_api_key


## Response:
??? question  "Example Response"

    === "Body"
        ``` { .json .select}
        {
          "data": {
            "assessing": {
              "area": 45,
              "city": "São Paulo",
              "lon": -46.7045881,
              "street_short": "iguatinga",
              "neighborhood_short": "santo amaro",
              "typology": {
                "features_garage": 1,
                "features_bathroom": 1,
                "features_bedroom": 1,
                "features_suite": 1
              },
              "number": null,
              "category_id": 1,
              "street": "R. Iguatinga",
              "sub_category_id": 1,
              "neighborhood": "Santo Amaro",
              "state": "SP",
              "postal_code": "04744-040",
              "complement": "apto 1202, bloco C",
              "lat": -23.6571986,
              "area_price": 8606.3
            },
            "search": {
              "is_sale": true,
              "max_age": 0,
              "area": {
                "useful": {
                  "min": 27,
                  "value": 45,
                  "max": 63,
                  "percentage": 40
                },
                "total": {
                  "min": 0,
                  "value": 0,
                  "max": 0,
                  "percentage": 100
                }
              },
              "typology": {
                "features_garage": [],
                "features_bathroom": [],
                "features_bedroom": [],
                "features_suite": []
              },
              "price_area": {
                "useful": {
                  "min": 0,
                  "value": 0,
                  "max": 0,
                  "percentage": 100
                },
                "total": {
                  "min": 0,
                  "value": 0,
                  "max": 0,
                  "percentage": 100
                }
              },
              "address": {
                "street_long": "Rua Iguatinga",
                "number": null,
                "city": "São Paulo",
                "street": "R. Iguatinga",
                "location": {},
                "neighborhood": "Santo Amaro",
                "state": "SP",
                "postal_code": "04744-040"
              },
              "realty_type": {
                "category_id": [
                  1,
                  2
                ],
                "sub_category_id": [
                  1,
                  2
                ]
              },
              "location": {
                "coordinates": [
                  []
                ],
                "lon": -46.7045881,
                "radius": 1500,
                "lat": -23.6571986
              },
              "price_total": {
                "min": 0,
                "value": 0,
                "max": 0,
                "percentage": 100
              }
            },
            "url_facade": null,
            "location": {
              "coordinates": [
                []
              ],
              "lon": -46.7045881,
              "radius": 1500,
              "lat": -23.6571986
            },
            "samples": [
              {
                "area": 48,
                "city_name": "São Paulo",
                "created_at": "2023-09-03T12:15:22.877Z",
                "features_bathroom": 2,
                "features_bedroom": 2,
                "features_garage": 1,
                "features_suite": 1,
                "link": "https://www.vivareal.com.br/imovel/imovel/apartamento-2-quartos-santo-amaro-zona-sul-sao-paulo-com-garagem-48m2-venda-RS423000-id-2632368783/",
                "link_key": "69fb409be819c59d828d301f78ba2395",
                "location_point": [
                  -46.704816,
                  -23.6568284
                ],
                "neighborhood_name": "Santo Amaro",
                "processed_address_formatted": "Rua Iguatinga, 230",
                "processed_address_number": "230",
                "processed_address_street": "Rua Iguatinga",
                "state_name": "São Paulo",
                "state_uf": "SP",
                "sub_category_id": 1,
                "total_area": 48,
                "updated_at": "2023-11-26T13:40:07.626Z",
                "similarity_index": 0.690625,
                "transaction": 423000,
                "sqrmeter_price_area": 8812.5,
                "sqrmeter_price_totalarea": 8812.5,
                "latest_update": "2023-11-26T13:40:07.626Z",
                "zip_code": "04744-040",
                "sqrmeter_price_area_adjusted": 8812.5,
                "sqrmeter_price_area_depreciated": 8107.5
              },
              {
                "area": 45,
                "city_name": "São Paulo",
                "created_at": "2023-11-16T06:49:22.648Z",
                "features_bathroom": 2,
                "features_bedroom": 2,
                "features_garage": 1,
                "features_suite": 1,
                "link": "https://www.vivareal.com.br/imovel/imovel/apartamento-2-quartos-santo-amaro-zona-sul-sao-paulo-com-garagem-45m2-venda-RS424367-id-2642815518/",
                "link_key": "e55f81b30d78d78f0e493eaa065d3ea6",
                "location_point": [
                  -46.704816,
                  -23.6568284
                ],
                "neighborhood_name": "Santo Amaro",
                "processed_address_formatted": "Rua Iguatinga, 230",
                "processed_address_number": "230",
                "processed_address_street": "Rua Iguatinga",
                "state_name": "São Paulo",
                "state_uf": "SP",
                "sub_category_id": 1,
                "total_area": 45,
                "updated_at": "2023-11-26T13:36:28.978Z",
                "similarity_index": 0.6901719761027658,
                "transaction": 424367,
                "sqrmeter_price_area": 9430.38,
                "sqrmeter_price_totalarea": 9430.38,
                "latest_update": "2023-11-26T13:36:28.978Z",
                "zip_code": "04744-040",
                "sqrmeter_price_area_adjusted": 9430.38,
                "sqrmeter_price_area_depreciated": 8675.9496
              },
              {
                "area": 45,
                "city_name": "São Paulo",
                "created_at": "2023-11-23T23:15:21.692Z",
                "features_bathroom": 1,
                "features_bedroom": 2,
                "features_garage": 1,
                "features_suite": 0,
                "link": "https://www.zapimoveis.com.br/imovel/venda-apartamento-2-quartos-com-piscina-santo-amaro-zona-sul-sao-paulo-sp-45m2-id-2670480712/",
                "link_key": "f0d9cea9a09181ea5fef589869ab9cb7",
                "location_point": [
                  -46.704816,
                  -23.6568284
                ],
                "neighborhood_name": "Santo Amaro",
                "processed_address_formatted": "Rua Iguatinga, 230",
                "processed_address_number": "230",
                "processed_address_street": "Rua Iguatinga",
                "state_name": "São Paulo",
                "state_uf": "SP",
                "sub_category_id": 1,
                "total_area": 45,
                "updated_at": "2023-11-29T08:09:47.312Z",
                "similarity_index": 0.6901281413880359,
                "transaction": 424500,
                "sqrmeter_price_area": 9433.33,
                "sqrmeter_price_totalarea": 9433.33,
                "latest_update": "2023-11-29T08:09:47.312Z",
                "zip_code": "04744-040",
                "sqrmeter_price_area_adjusted": 9433.33,
                "sqrmeter_price_area_depreciated": 8678.6636
              },
              {
                "area": 46,
                "city_name": "São Paulo",
                "created_at": "2023-03-05T10:09:23.585Z",
                "features_bathroom": 2,
                "features_bedroom": 2,
                "features_garage": 1,
                "features_suite": 1,
                "link": "https://www.zapimoveis.com.br/imovel/venda-apartamento-2-quartos-com-piscina-santo-amaro-zona-sul-sao-paulo-sp-46m2-id-2616258316/",
                "link_key": "f9f88952edfc7168614042522f8a16b3",
                "location_point": [
                  -46.704816,
                  -23.6568284
                ],
                "neighborhood_name": "Santo Amaro",
                "processed_address_formatted": "Rua Iguatinga, 230",
                "processed_address_number": "230",
                "processed_address_street": "Rua Iguatinga",
                "state_name": "São Paulo",
                "state_uf": "SP",
                "sub_category_id": 1,
                "total_area": 46,
                "updated_at": "2023-11-26T02:22:19.838Z",
                "similarity_index": 0.6847595559666975,
                "transaction": 373000,
                "sqrmeter_price_area": 8108.7,
                "sqrmeter_price_totalarea": 8108.7,
                "latest_update": "2023-11-26T02:22:19.838Z",
                "zip_code": "04744-040",
                "sqrmeter_price_area_adjusted": 8108.7,
                "sqrmeter_price_area_depreciated": 7460.004
              },
              {
                "area": 48,
                "city_name": "São Paulo",
                "created_at": "2023-11-16T06:49:40.588Z",
                "features_bathroom": 2,
                "features_bedroom": 2,
                "features_garage": 1,
                "features_suite": 1,
                "link": "https://www.vivareal.com.br/imovel/imovel/apartamento-2-quartos-santo-amaro-zona-sul-sao-paulo-com-garagem-48m2-venda-RS445390-id-2642815519/",
                "link_key": "1787e1c63b5965a2d00c974c95403f03",
                "location_point": [
                  -46.704816,
                  -23.6568284
                ],
                "neighborhood_name": "Santo Amaro",
                "processed_address_formatted": "Rua Iguatinga, 230",
                "processed_address_number": "230",
                "processed_address_street": "Rua Iguatinga",
                "state_name": "São Paulo",
                "state_uf": "SP",
                "sub_category_id": 1,
                "total_area": 48,
                "updated_at": "2023-11-26T13:35:46.730Z",
                "similarity_index": 0.6830843920008277,
                "transaction": 445390,
                "sqrmeter_price_area": 9278.96,
                "sqrmeter_price_totalarea": 9278.96,
                "latest_update": "2023-11-26T13:35:46.730Z",
                "zip_code": "04744-040",
                "sqrmeter_price_area_adjusted": 9278.96,
                "sqrmeter_price_area_depreciated": 8536.643199999999
              }
            ],
            "final_price": 387283.34,
            "is_sattelite": false,
            "statistics": {
              "total_samples": 5,
              "sqrmeter_average_thousand": 9012.774,
              "sqrmeter_average_one_hundred": 9012.774
            }
          },
          "message": "Os dados do Laudo de Avaliação de Imóveis foram encontrados com sucesso!",
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
    
