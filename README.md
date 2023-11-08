Modelo Preditivo - Fraude Bancária
O objetivo desta análise é identificar uma possível fraude com base nos dados de pessoas de cada cliente, como idade, renda, risco de crédito e etc. Um dos maiores desafios deste conjunto de dados é o desbalanceamento de classes porque existem mais transações legais do que transações com algum tipo de fraude. Outro ponto a ser destacado é que esse é um tipo de problema que tende a ter um retorno muito alto para instituições financeiras visto que a partir da identificação de uma suspeita de fraude, a instituição pode tomar decisões rápidas e objetivas evitando o prejuízo ou mesmo evitando o risco do mesmo. De acordo com o InfoMoney em uma reportagem de Ago/22, golpes bancários têm potencial de gerar um prejuízo de R$ 2,5 BI em 2022.

Fonte reportagem: https://www.infomoney.com.br/minhas-financas/golpes-bancarios-disparam-e-devem-gerar-prejuizos-de-r-25-bilhoes-neste-ano/

Informações do conjunto de dados
O conjunto de dados de Fraude de Conta Bancária (BAF) foi publicado no NeurIPS 2022 e compreende um total de 6 conjuntos de dados tabulares de fraude de conta bancária sintética diferentes. O BAF é um banco de teste realista, completo e robusto para avaliar métodos novos e existentes em ML, e o primeiro de seu tipo!

Este conjunto de dados é:

Realista, baseado em um conjunto de dados do mundo real atual para detecção de fraudes;
Tendencioso, cada conjunto de dados tem diferentes tipos de viagens controladas;
Desequilibrado, esse cenário apresenta baixíssima prevalência de classe positiva;
Dinâmico, com dados temporais e mudanças de distribuição observadas;
Preservando a privacidade, para proteger a identidade dos candidatos em potencial, aplicamos técnicas de privacidade diferencial (adição de ruído), modificadas de recursos e treinamos um modelo generativo (CTGAN).
O conjunto de dados foi disponibilizado no Kaggle de maneira pública.

Fonte do conjunto de dados: https://www.kaggle.com/datasets/sgpjesus/bank-account-fraud-dataset-neurips-2022

Dicionário de Dados
Atributo	Descrição	Métrica
fraude bool	Marcador de Fraude	1 se é fraude, 0 se é legítimo
renda	Renda anual das aplicações em quartis	Valores entre [0, 1]
nome_email_similaridade	Métrica de semelhança entre e-mail e nome de quem aplicou. Quanto maior o valor, maior a similaridade	Valores entre [0, 1]
prev_address_months_count	Número de meses registrados no endereço de quem aplicou, em outras palavras a residência anterior de quem apliccou, se disponível	Valores entre [−1, 380] meses (-1 para valores faltando)
current_address_months_count	Meses que o solicitante está registrado no endereço atual	Valores entre [−1, 406] meses (-1 para valores faltando)
idade_do_cliente	Idade do requerente segmentada por décadas (exemplo, 20-29 é representada como 20)	Categórico
dias_desde_solicitação	Número de dias que passaram desde que a aplicação foi feita	Valores entre [0, 78] dias
valor_balcão_intencionado	Qauntidade detalhada inicialmente	Valores entre [−1, 108]
tipo de pagamento	Tipo de plano de crédito	5 valores possíveis (anônimo)
zip_count_4w	Número de aplicações com o mesmo código postal nas últimas 4 semanas	Valores entre [1, 5767]
velocidade_6h	Velocidade do total de aplicações realizadas nas últimas 6 horas, ou seja, número médio de aplicações por hora nas últimas 6 horas	Variação entre [−211, 24763]
velocidade_24h	Velocidade do total de aplicações realizadas nas últimas 24 horas, ou seja, número médio de aplicações por hora nas últimas 24 horas	Varia entre [1329, 9527]
velocidade_4w	Velocidade do total de aplicações realizadas nas últimas 4 semanas, ou seja, número médio de aplicações por hora nas últimas 4 semanas	Varia entre [2779, 7043]
banco_branch_count_8w	Número total de aplicações na agência bancária selecionada nas últimas 8 semanas	Variação entre [0, 2521]
data_de_nascimento_distinct_emails_4w	Número de e-mails para candidatos com a mesma data de nascimento nas últimas 4 semanas	Variação entre [0, 42]
situação de emprego	Situação profissional do requerente	7 valores possíveis (anônimos)
pontuação_de_crédito_risco	Pontuação interna de risco do aplicativo	Varia entre [−176, 387]
email_is_free	Domínio do e-mail do aplicativo	gratuito ou pago
Status da moradia	Situação residencial atual do solicitante	7 valores possíveis (anônimos)
telefone_home_valid	Validade do telefone residencial fornecido	Categórico (1, 0)
telefone_celular_válido	Validade do telefone celular fornecido	Categórico (1, 0)
banco_meses_contagem	Quantos anos tem a conta anterior (se mantida) em meses	Varia entre [−1, 31] meses (-1 para valores faltando)
tem_outros_cartões	Se o requerente tiver outros cartões da mesma empresa bancária	Categórico
limite_de_crédito proposto	Limite de crédito solicitado pelo requerente	Varia entre [200, 2000]
solicitação_estrangeira	se o país de origem do pedido for diferente do país do banco	Categórico (1, 0)
fonte	Fonte online de aplicação	Navegador (INTERNET) ou aplicativo móvel (APP)
session_length_in_minutos	Duração da sessão do usuário no site bancário em minutos	Variação entre [−1, 107] minutos
dispositivo_os	Sistema operacional do dispositivo que fez o pedido	Os valores possíveis são: Windows, Mac, Linux, X11 ou outro
keep_alive_session	Opção do usuário ao sair da sessão	Categórico (1, 0)
device_distinct_emails_8w	Número de e-mails diferentes no site bancário do dispositivo usado nas últimas 8 semanas	Variação entre [0, 3]
contagem_de_fraude_de_dispositivos	Número de aplicativos fraudulentos com dispositivo usado	Variação entre [0, 1]
mês	Mes em que foi feito o pedido	Variação entre [0, 7]
Informações do conjunto de dados:

Total de Registros	1.000.000
Total de Atributos	32
