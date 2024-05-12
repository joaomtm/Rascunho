## Sumário

[1. Introdução e Contexto](#c1)

[2. Metodologia Utilizada](#c2)

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
O dado em questão é o hubspot disponibilizado pela Wizard, dando detalhes específicos sobre o comportamento do usuário na landing page na sua jornada de se tornar um lead. Ao total, a tabela contém 46 colunas e cerca de 52 mil linhas.

Para a construção das simulações 4 colunas foram utilizadas: Became a Lead Date (registra a data em que um visitante se tornou um lead), Number of Sessions (indica quantas vezes um visitante acessou o site em um determinado período.), Number of Pageviews (contabiliza o total de visualizações de página durante as sessões dos visitantes) e Number of Form Submissions (registra quantas vezes os formulários do site foram preenchidos e enviados pelos visitantes).

Essas quatro colunas foram selecionadas entre as 42 disponíveis, levando em consideração o objetivo central do projeto: aumentar a taxa de conversão de leads. Assim, selecionamos as colunas que se referem diretamente às datas da conversão de lead (Became a Lead Date), o número de leads convertidos (Number of Form Submissions) e características do uso desse lead (Number of Sessions e Number of Pageviews). Todos os dados dessas colunas são ideais para a definição  de variáreis na Simulação de Monte Carlo, sendo extremamente quantitativos os dados das três últimas colunas, o que permite desenvolver comparações minuciosas e análises temporais. 

As outras colunas não foram utilizadas para o desenvolvimento da simulações por serem voltadas  para uma área de marketing avançada, fugindo do escopo do projeto (ex: Google ad click id). Outras colunas também aumentavam demais a granularidade das informações e não contribuiam para a análise quantitativa dos dados (ex: IP City).













  


- [Documentação do Framework HEART para WizardOn](https://github.com/Inteli-College/2024-1B-T04-SI10-G02/blob/develop/document/Sprint%2001/HEART.md)

