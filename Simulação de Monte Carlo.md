## Sumário

[1. Introdução e Contexto](#c1)

[2. Setup (Bibliotecas e Impotação de Dados)](#c2)

[2. Simulações de Monte Carlo](#c3)

<br>


# <a name="c1"></a>1. Introdução e Contexto

&emsp;&emsp; A simulação de Monte Carlo é uma técnica estatística que se baseia na geração de números aleatórios para modelar fenômenos complexos ou sistemas cujo comportamento não pode ser facilmente previsto por
métodos analíticos tradicionais. Ela foi originalmente desenvolvida pelo matemático Stanislaw Ulam, tendo aplicações no campo da física, engenharia, finanças e biologia. A essência dessa técnica é realizar uma grande quantidade de experimentos virtuais,onde parâmetros importantes são selecionados aleatoriamente dentro de intervalos conhecidos, permitindo assim a obtenção de estimativas probabilísticas de resultados. Isso proporciona insights valiosos sobre o comportamento de sistemas complexos e a probabilidade de ocorrência de eventos específicos. No atual projeto com a Wizard, o sistema complexo que se deseja analisar é o comportamento dos 
usuários na Landing Page da Wizard On. Os parâmetros utilizados são definidos a partir dos dados disponiblizados pela própria Wizard (vistos na análise preliminar desse mesmo projeto). Nesse documento será detalhado o desenvolvimento das simulações de Monte Carlo, incluindo a construção precisa dos modelos, a escolha dos parâmetros e a execução das iterações. Além disso, serão analisados os resultados gerados pela simulação e suas implicações para otimização da Landing Page. As simulações foram feitas em dois arquivos python (.ipynb), por conterem a mesma estrutura básica, eles serão detalhados de forma única nesse documento. 


# <a name="c2"></a>2. Setup (Bibliotecas e Impotação de Dados)

- Bibliotecas
  
  ![image](https://github.com/joaomtm/Rascunho/assets/99208815/38dcb6c1-d6f5-475b-8c2f-66550a897159)

O Pandas é a principal biblioteca análise de dados em Python, oferecendo estruturas como o DataFrame, que simplificam a manipulação de dados tabulares.O Plotly Express é uma ferramenta de alto nível que facilita a criação rápida de gráficos interativos, tornando a visualização de dados complexos mais acessível. Já o NumPy, ele desempenha um papel fundamental na computação numérica, fornecendo suporte para arrays multidimensionais e operações matemáticas eficientes. Já o Matplotlib.pyplot, é uma biblioteca para visualização estática de dados em Python, oferecendo uma variedade de gráficos. Essas biblotecas servirão de apoio à Simulação de Monte Carlo, disponibilizando dados, ajudando na construção de modelos e na visualização de resultados.

- Importação de Dados
  
![image](https://github.com/joaomtm/Rascunho/assets/99208815/3665890c-d721-4b97-a9e5-3b73906619a2)

Os dados são importados pelo método pandas, lendo diretamente um csv armazenado no Google Drive.
O dado em questão é o hubspot disponibilizado pela Wizard, dando detalhes específicos sobre o comportamento do usuário na landing page, sua características e jornada até se tornar um lead. Ao total, a tabela contém 46 colunas e cerca de 52 mil linhas.

Para a construção das simulações 4 colunas foram utilizadas: Became a Lead Date (registra a data em que um visitante se tornou um lead), Number of Sessions (indica quantas vezes um visitante acessou o site em um determinado período.), Number of Pageviews (contabiliza o total de visualizações de página durante as sessões dos visitantes) e Number of Form Submissions (registra quantas vezes os formulários do site foram preenchidos e enviados pelos visitantes).

Essas quatro colunas foram selecionadas entre as 42 disponíveis, levando em consideração o objetivo central do projeto: aumentar a taxa de conversão de leads. Assim, selecionamos as colunas que se referem diretamente às datas da conversão de lead (Became a Lead Date), o número de leads convertidos (Number of Form Submissions) e características do uso desse lead (Number of Sessions e Number of Pageviews). Todos os dados dessas colunas são ideais para a definição  de variáreis na Simulação de Monte Carlo, sendo extremamente quantitativos os dados das três últimas colunas, o que permite desenvolver comparações minuciosas e análises temporais. 

As outras colunas não foram utilizadas para o desenvolvimento da simulações por serem voltadas  para uma área de marketing avançada, fugindo do escopo do projeto (ex: Google ad click id). Outras colunas também aumentavam demais a granularidade das informações e não contribuiam para a análise quantitativa dos dados (ex: IP City).

# <a name="c3"></a>3. Simulações de Monte Carlo
## Simulações Macro

As primeiras simulações realizadas são feitas em um escopo macro, não considerando um período de campanha específico, mas sim de todos os anos. O objetivo é analisar o comportamento geral dos usuários na Landing Page como um todo e identificar padrões ou tendências que possam influenciar a conversão de leads. Essas simulações ajudarão a entender melhor o contexto geral e a direcionar análises mais detalhadas.

- Simulação 1: "Coluna "Number of Form Submissions"

![image](https://github.com/joaomtm/Rascunho/assets/99208815/7bcff987-8549-4922-848e-7f675eec1158)

![image](https://github.com/joaomtm/Rascunho/assets/99208815/81e650c5-6dc1-416c-9827-cb74c92d0221)

Essa primeira parte do código realiza pré-processamento e análise de um DataFrame df com dados de leads da Wizard. Primeiro, converte a coluna 'Became a Lead Date' para o formato datetime. Em seguida, divide os dados em duas partes com base na data '2024-04-18', data em que o botão do Whatssap foi incluído na Landing Page. Calcula o maior e o menor número de formulários submetidos antes e depois dessa data. A partir desses dados, é possível observar que existem casos de envio de mais de um formulário, sendo que o primeiro período de tempo contém um grande outlier (401).

![image](https://github.com/joaomtm/Rascunho/assets/99208815/6864c368-decf-4d36-9ed0-566c91810969)

Esse código define uma função chamada remove_outliers que remove outliers de um conjunto de dados usando a técnica do intervalo interquartil (IQR). Primeiro, calcula os quartis Q1 e Q3 e, em seguida, calcula o IQR. Com base nesses valores, determina os limites inferior e superior para identificar outliers. Em seguida, filtra os dados para manter apenas aqueles que estão dentro desse intervalo. A função retorna os dados sem outliers.Depois, o código aplica essa função aos dados de formulários submetidos antes e depois de uma determinada data, armazenando os resultados em duas variáveis separadas. Em seguida, combina esses resultados em um único conjunto de dados, removendo outliers de todos os dados de formulários submetidos.


![image](https://github.com/joaomtm/Rascunho/assets/99208815/892792b1-f96a-4175-b625-5d9eebfa876c)


Esse código gera um histograma para visualizar a distribuição do número de formulários submetidos, excluindo outliers. Primeiro, ele calcula o histograma usando os dados sem outliers e especifica o número de bins desejado. Em seguida, calcula as porcentagens de cada bin em relação ao total de dados e cria um gráfico de barras com essas porcentagens em relação aos bins.

O gráfico resultante mostra a distribuição dos formulários submetidos, destacando a proporção de dados em cada intervalo. Isso permite uma visualização clara da concentração dos formulários submetidos em diferentes faixas de valores.

![image](https://github.com/joaomtm/Rascunho/assets/99208815/8779ce8a-dfb6-4e7e-b837-4556f1723a2a)

Este código realiza a simulação de Monte Carlo em si. Primeiro, define-se uma função simulacao() que recebe um valor e simplesmente o retorna. Em seguida, cria-se um array e um array de probabilidades associadas a cada valor do array. Depois, define-se o número de simulações desejadas (no caso, serão feitas 100 simulações)

Dentro de um loop, para cada simulação, uma amostra é retirada aleatoriamente do array com base nas probabilidades especificadas. A função simulacao() é então chamada com essa amostra como argumento, e o resultado é armazenado em uma lista de resultados de simulação.

Por fim, um histograma é criado com base nos resultados das simulações.

- Gráficos gerados: 

![image](https://github.com/joaomtm/Rascunho/assets/99208815/9907cee7-1cfc-478a-9c2a-5dcaef58f53c)

![image](https://github.com/joaomtm/Rascunho/assets/99208815/030d1ea1-844d-4317-add3-6df120bd63b5)

A observação dos gráficos gerados revela que a distribuição aleatória produzida pela simulação segue o mesmo padrão observado no gráfico construído diretamente com os dados originais. Isso confirma a consistência do padrão e das proporções das distribuições. Analizando as colunas, é possível concluir que a maioria dos usuários enviam pelo menos dois formulários de inscrição. Pode-se supor então que os usuários não sentem uma mensagem de confirmação de inscrição ao preencherem o formulário, preenchendo-o mais de uma vez para talvez "garantirem que de fato se inscreveram". Esse fator pode ser um indício de que o campo do formulário não transmite uma sensação de confirmação ou compromisso, fazendo possivelmente potenciais leads saírem da página ao não identificarem ou sentirem que de fato começaram o processo de integração no curso. Outra hipótese é que de alguma forma um preenchimento de formulário está gerando um resultado duplicado, afetando análises como essa.

- Simulação 2: Coluna "Number of Pageviews"

![image](https://github.com/joaomtm/Rascunho/assets/99208815/96cad9c7-b45e-49a0-80f7-7d30bd534e58)

Este trecho de código calcula o maior e o menor valor do número de visualizações de página. É possível perceber que no primeiro período (antes do botão do Whatssap ser aplicado na Landing Page), há outliers (2061).

![image](https://github.com/joaomtm/Rascunho/assets/99208815/cac9842d-d662-4ac0-bfe3-15d48cb1e92d)

![image](https://github.com/joaomtm/Rascunho/assets/99208815/f6132cdb-211d-4459-9d05-b14a904ef428)



 

