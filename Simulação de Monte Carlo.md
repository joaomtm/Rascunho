## Sumário

[1. Introdução e Contexto](#c1)

[2. Metodologia Utilizada](#c2)

<br>


# <a name="c1"></a>1. Introdução e Contexto

&emsp;&emsp; A simulação de Monte Carlo é uma técnica estatística que se baseia na geração de números aleatórios para modelar fenômenos complexos ou sistemas cujo comportamento não pode ser facilmente previsto por
métodos analíticos tradicionais. Ela foi originalmente desenvolvida pelo matemático Stanislaw Ulam, tendo aplicações no campo da física, engenharia, finanças e biologia. A essência dessa técnica é realizar uma grande quantidade de experimentos virtuais,onde parâmetros importantes são selecionados aleatoriamente dentro de intervalos conhecidos, permitindo assim a obtenção de estimativas probabilísticas de resultados. Isso proporciona insights valiosos sobre o comportamento de sistemas complexos e a probabilidade de ocorrência de eventos específicos. No atual projeto com a Wizard, o sistema complexo que se deseja analisar é o comportamento dos 
usuários na Landing Page da Wizard On. Os parâmetros utilizados são definidos a partir dos dados disponiblizados pela própria Wizard (vistos na análise preliminar desse mesmo projeto). Nesse documento será detalhado o desenvolvimento das simulações de Monte Carlo, incluindo a construção precisa dos modelos, a escolha dos parâmetros e a execução das iterações. Além disso, serão analisados os resultados gerados pela simulação e suas implicações para otimização da Landing Page. As simulações foram feitas em dois arquivos python (.ipynb), por conterem a mesma estrutura básica, eles serão detalhados de forma única nesse documento. 


# <a name="c2"></a>2. Setup (Biblioteca e Dados)

- Bibliotecas
  ![image](https://github.com/joaomtm/Rascunho/assets/99208815/38dcb6c1-d6f5-475b-8c2f-66550a897159)

  


- [Documentação do Framework HEART para WizardOn](https://github.com/Inteli-College/2024-1B-T04-SI10-G02/blob/develop/document/Sprint%2001/HEART.md)

