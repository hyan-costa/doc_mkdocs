# **Introdução**

## AVM

A Agile Valuation Model (AVM) é uma api automatizada de avaliações de imóveis. O AVM seleciona as melhores amostras
usando o I. S. (Índice de Similaridade) ao Avaliando. Tecnologia proprietária que leva em consideração múltiplas
frentes, características e rating do imóvel.

## Informações Gerais

Dois ambiente estão sendo disponibilizados, qa e prd. Cada ambiente tem sua **`x-api-key`**, ela é única e pessoal equivalente
a uma senha, logo é recomendado cuidado para não expor na hora de utilizar.

## Como consumir

A primeira rota a ser chamada é a "iniciar avaliação". Nela é passado os dados do seu avaliando e dados dos imoveis
que vão servir de comparação.

* `/avm-gateway/internal/start_valuation`

!!! note

    Seu retorno é a chave de identificação da avaliação, esse id vai ser usado para consultar qualquer informação 
    relativa a essa avaliação


## Resumo individual de Cada Endpoint


Na rota abaixo é possível verificar o estado em que a avaliação se encontra, como verificar se as amostras já foram selecionadas ou se ocorreu algum erro durante o processo de avaliação.

* `/avm-gateway/internal/get_valuation_status/id_avaliação`

Quando o status de preço vir completo na rota de obter status, significa que a avaliação foi finalizada e a rota de 
"obter avaliação" já pode ser chamada. Onde o seu retorno traz todos os dados da avaliação.

   * `/avm-gateway/internal/get_valuation/id_avaliação`


Quando o status de preço vir compleato na rota de obter status significa que a avaliação foi finalizada e a rota de 
"obter avaliação" já pode ser chamada, onde o seu retorno traz todos os dados da avaliação.

  * `/avm-gateway/internal/get_valuation/id_avaliação`


E por último a rota de obter laudo, apresenta os mesmos dados que o endpoint anterior porem em formato de pdf, atraves de uma url pré-assinada.

  * `/avm-gateway/internal/get_report_pdf/id_avaliação`

!!! warning 

    Todas as rotas exigem a chave **`x-api-key`** no header da requisição.


## Visualizar Avaliação

Além de conseguir obter os dados do laudo e/ou seu pdf via endpoint, também disponibilizamos uma página web já pronta para
visualização de qualquer avaliação já precificada pela api.

### Homologação (qa):

   * `https://avm-qa.valuation.eemovel.com.br/laudo/seu_id_aqui`

### Produção (prd):

   * `https://avm.valuation.eemovel.com.br/laudo/seu_id_aqui`


!!! note

    Para visualização, basta substituir a parte final das urls a cima pelo id retornado na rota de iniciar avaliação.



