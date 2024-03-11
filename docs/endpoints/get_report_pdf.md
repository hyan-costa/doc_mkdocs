# **GET** Report Valuation


## Rota:
    https://api.prd.valuation.eemovel.com.br/admin/avm-gateway/internal/get_report_pdf/54e919851bb94c32b00670dc53751022



### Retorna um link pré-assinado, que ao fazer uma requisição get nesse link o pdf do laudo será obtido.



## Request:
??? question  "Example Request"
    * *method: GET*
    === "Request"
            curl --location 'https://api.prd.valuation.eemovel.com.br/admin/avm-gateway/internal/get_report_pdf/b48387c642ec45c0b0e007b96f3076bd' --header 'x-api-key: apikey'
    === "Headers (1)"
             x-api-key                               your_api_key


## Response:
??? question  "Example Request"

    === "Body"
        ``` { .json .select}
        { 
          "data": "https://qa-platform-assessment-reports.s3.amazonaws.com/e1600b0189beba9325bb868e9f8517b8/b48387c642ec45c0b0e007b96f3076bd/assessment/b48387c642ec45c0b0e007b96f3076bd.pdf?AWSAccessKeyId=ASIAWNUKNJ6OC4Z7GM6Z&Signature=YZo4rcZCNzx1SLVZrHm9ozv9%2Bsc%3D&x-amz-security-token=IQoJb3JpZ2luX2VjEIj%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJHMEUCIQCVPJkv1gU1R1P6DNaBrvbXPP5oCkwalYHLps1nYR0ehgIgcUjvugpiQOq0nWiS2S6V3yA0Y8kPC5AZhocA3ZwtIHcqsgMI4f%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FARABGgw0NDE1OTgxNjg5ODgiDGXpHAHuusSETOMAaCqGA1MympO31uj6CVkiO3roCgZvbnjQLYlb79i1y3T1iu%2BjfXXPvsbRrxJgOe1DLTYp8bJI411YptWlDdHaZv816lAU6w9ZWyeY9VuvaC7Jf1Lta7W8kF%2B%2BhYz54mCfJrzddhMSPm5CApFFOwr9bX%2FDedZFnn2ynMgcWrYZAlFWcZBokTx1MoBC6NQZEUix%2FLVV8CpMWdrtyH4oVvCTzcNFJ1YjqntYUzvCwNiiJLbh3GlZsa3kGJZM1yzyyi%2FgiAeoxG7aoo6ac%2Fbg2%2FjMxni3nz0BCH9qZZXLWDrsobAR8pelQ2WQ4i8TGmo8mmxbGY7Y3olaP2IwN2FQT%2B1ra5UVvxURc0eaidkLVtq1LpA1avM18WiOV9gYeMK7Mc9bxOkNTYf6QhEmaYmBpRNpyYefU93iqzBNfhyOlyVg16RVTyvKu6%2B%2FwQcNveraioKJnNeOQeNpjd%2Bi1g5fMebdD83M6ui51oLF29gWrAzf3rbQODK4jmLbEDJLPfC2ZMynfVIoO7Eh%2FuWWmjCpmp%2BrBjqdAfS922qvjTLx5fEOYbaJOXEOGrQw6RBgDjxuIw8hccpbBOHTwefyWVR7r%2FV9wDfLLel9jg%2FOLZ1Zm6w%2BOvFuG%2FTocHhvUit49C2nATVr%2BP6RsJMm%2BvKtQRtftZJ%2BmTkisipGMADtIhbBIWVNxkADH5wX8ipX1GqoZijm4lAD86rU%2BIN5af1FRqnPudUbs7ytMWxphzYHPqx4N2rbR3E%3D&Expires=1701301614",
          "message": "Os dados do Laudo de Avaliacao de Imoveis foram encontrados com sucesso!",
          "code": 200,
          "success": true
        }
        ```

    === "Headers (13)"
             x-api-key                               your_api_key

