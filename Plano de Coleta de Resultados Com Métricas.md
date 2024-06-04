# Plano de Coleta de Resultados Com Métricas

## Objetivo 

&emsp;&emsp; Este segmento da documentação tem como objetivo detalhar o plano proposto para a coleta de resultados do teste A/B. Quando as telas Bs forem aplicadas no site da Wizard On, diversos dados serão gerados e armazenados. Contudo, é crucial definir quais desses dados de fato representam boas métricas para avaliarmos o desempenho das novas telas propostas. Assim, será desenvolvido um plano para uma minuciosa coleta de resultados que futuramente permitirá uma análise preliminar dessa apuração.


## Fonte Inicial de Dados, Looker Studio Google

&emsp;&emsp; O Looker Studio é uma ferramenta de visualização de dados e criação de relatórios interativos oferecida pelo Google. Para este projeto, a Pearson configurou diretamente o Looker para acessar os dados coletados atualmente pelos endereços de site referentes à Wizard On. Para esta análise preliminar e para o primeiro plano de coleta de resultados, apenas essa fonte primária do Looker será considerada.

<p align="center">
  <img src="https://github.com/joaomtm/Rascunho/assets/99208815/9a79aba1-e097-410e-ae11-f38cbede1b40" alt="image">
</p>



![image](https://github.com/joaomtm/Rascunho/assets/99208815/e1639553-bbcd-457e-bb26-d71c9ad7c49f)



### Remoção do Número de Telefone 
**Tela A:**
![image](https://github.com/joaomtm/Rascunho/assets/99208815/de705c61-41bc-44fe-b27e-b0b74142c029)
**Tela B:**
![image](https://github.com/joaomtm/Rascunho/assets/99208815/704a0802-9923-4670-a4ef-b24a78f82b9b)

&emsp;&emsp; Assumimos em nossas hipóteses de que o número de telefone não era mais essencial e não contribuía para a conversão de inscrições e leads. Essa hipótese se baseia principalmente na informação que temos da persona, que são mulheres jovens na faixa de 25 anos. Contudo, mesmo a persona utilizada sendo a pessoa média que usa o serviço, ainda existem os usuários atípicos, que tanto podem ser pessoas bem mais velhas que ainda possuem o costume de ligar para o estabelecimento ou até mesmo pessoas jovens que fortemente preferem fazer ligações quando desejam contratar um serviço. Assim, existe o risco da nova tela B ter menos inscrições e gerar menos leads por excluir um meio de comunicação e inscrição. Contudo, esse cenário é altamente improvável (conforme a "We Social" 93,4% dos brasileiros com acesso à internet usam WhatsApp) e de baixo impacto (estamos considerando um usuário que está fora da persona).


### Alteração de Texto no Botão de Envio do Formulário 
**Tela A:** 
![image](https://github.com/joaomtm/Rascunho/assets/99208815/000832d6-a889-431a-918b-b4719b8c3161)
**Tela B:**
![image](https://github.com/joaomtm/Rascunho/assets/99208815/b6148190-f6df-4485-8f8a-b65272971f4a)


&emsp;&emsp; O risco dessa mudança de textos nos botões envolve a perda do valor de urgência. O texto "enviar" agrega valor no aspecto técnico, na clareza das ações que o usuário deve tomar para enviar o formulário. Porém, "aproveite!" agrega um apelo emocional e de urgência, incentivando a ação imediata. Assim, é possível que essa mudança provoque a diminuição de cliques no envio de formulário e, por consequência, a taxa de conversão e inscrições diminuia. A probabilidade desse risco é baixa, mesmo tendo esse aspecto emocional e de urgência, o texto "aproveite!" perde parte do seu apelo por ser usado de forma massiva nas publicidades, contudo, talvez seja subestimar demais essa fórmula. O impacto deste risco seria médio, se esse ele se concretizasse, um pequeno número de potenciais clientes poderia ser perdido.






