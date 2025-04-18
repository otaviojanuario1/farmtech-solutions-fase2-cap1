# farmtech-solutions-fase2-cap1
Repositório do projeto de modelagem MER/DER - FarmTech Solutions
Item 1 – Informações Relevantes e Dados Necessários
Para atender às necessidades do produtor rural e garantir um sistema eficiente de armazenamento e análise dos dados agrícolas, foram identificadas as seguintes informações e os respectivos dados necessários:

a) Monitoramento da aplicação de água
Informações relevantes:

A quantidade total de água aplicada na plantação ao longo do tempo;

Quando e onde foi realizada cada aplicação.

Dados necessários:

Data e hora do ajuste de aplicação de água;

Quantidade de água aplicada (em litros);

Identificação da área da plantação onde a água foi aplicada;

Sensor responsável pela coleta das informações (sensor de umidade – S1).

b) Acompanhamento dos níveis de pH do solo
Informações relevantes:

Variação do pH do solo ao longo do ano;

Picos de acidez ou alcalinidade nas diferentes áreas da plantação.

Dados necessários:

Data e hora das leituras do sensor de pH (S2);

Valor de pH registrado;

Localização ou identificação da área onde a leitura foi feita.

c) Monitoramento da concentração de nutrientes (P e K)
Informações relevantes:

Quantidade de fósforo (P) e potássio (K) no solo;

Necessidade de ajuste ou reforço na aplicação de fertilizantes.

Dados necessários:

Data e hora da leitura do sensor de nutrientes (S3);

Valor de fósforo (P) registrado;

Valor de potássio (K) registrado;

Área da plantação onde os dados foram coletados.

d) Histórico de dados para previsões
Informações relevantes:

Comportamento dos dados ao longo do tempo;

Correlações entre aplicação de água, nutrientes e resultados da colheita.

Dados necessários:

Registros históricos de leituras dos sensores (S1, S2 e S3);

Dados de aplicação de água e nutrientes;

Informações sobre a cultura plantada em cada área;

Resultados de produção colhida.
Item 2 - Entidades e Atributos (MER)
As seguintes entidades foram definidas para representar os elementos essenciais do sistema da FarmTech Solutions, com seus respectivos atributos:

1. Produtor

id_produtor (PK)

nome

cpf

telefone

2. Plantação

id_plantacao (PK)

localizacao

area_total

data_inicio

id_produtor (FK)

3. Cultura

id_cultura (PK)

nome

tipo

tempo_estimado_colheita

4. Sensor

id_sensor (PK)

tipo_sensor (umidade, pH, nutrientes)

marca

modelo

id_plantacao (FK)

5. LeituraSensor

id_leitura (PK)

data_hora

valor_umidade

valor_ph

valor_fosforo

valor_potassio

id_sensor (FK)

6. AjusteAplicacao

id_ajuste (PK)

data_hora_ajuste

quantidade_agua

quantidade_nutrientes

id_plantacao (FK)

