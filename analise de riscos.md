# Análise de Riscos

## Objetivo 

&emsp;&emsp; O objetivo dessa análise de riscos é identificar e avaliar os possíveis riscos associados à implementação da tela B (teste) no site da Wizard On e, diante disso, desenvolver estratégias e propostas para mitigar ou lidar com os riscos identificados.
Esse fator de risco está intimamente associado aos testes A/B (como o próprio nome diz, um teste), pois todas as mudanças propostas são apenas hipóteses, que mesmo embasadas em dados quantitativos e/ou qualitativos, ainda sofrem da 
possibilidade de serem falsas. Assim, este documento buscará detalhar esse potencial mau cenário e sugerir ações diante dele. 

## Identificação e Avaliação de Possíveis Riscos

&emsp;&emsp; Nessa seção será identificado as mudanças feitas na página e os possíveis riscos associados à elas. As mudanças da versão mobile e desktop são de extrema semelhança, assim, os riscos associados foram os mesmos.

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


### Alteração Visual e de Localização do Botão Whatsapp  
**Tela A:** 
![image](https://github.com/joaomtm/Rascunho/assets/99208815/95708ade-c9c9-4dec-93d9-23ebf4d88495)
**Tela B:**
![image](https://github.com/joaomtm/Rascunho/assets/99208815/1f0b56f2-e117-4a56-8930-58d091939b33)



&emsp;&emsp; Sendo uma das alterações mais críticos do teste B, a diminuição, redesign e nova localização do botão do WhatsApp pode provocar uma diminuição significativa da conversão de leads. Segundo os gestores da Wizard, hoje o botão do WhatsApp é o principal meio de conversão de cliques e inscrições. Nossa hipótese é que esse botão está demasiadamente grande, atrapalhando a leitura de outras informações na página, interação com o formulário e gerando até "miss clicks" (cliques falsos) na versão mobile. O risco está na equilíbrio dessas alterações do botão, existe a possibilidade dele ficar muito discreto (pouco chamativo, que não gera a iniciativa de interação), perdendo esse grande número de usuários que se convertem a partir desse meio. Portanto, essa alteração contém um risco médio com impactos altos. 


### Alteração do Texto Referente às Vantagens Associadas ao Curso
**Tela A:**

![image](https://github.com/joaomtm/Rascunho/assets/99208815/8699604f-8182-44e3-8308-a634c8a87b6f)

**Tela B:**

![image](https://github.com/joaomtm/Rascunho/assets/99208815/af025b98-d4ab-472a-8ea8-1020598b0746)


&emsp;&emsp; A alteração feita está diretamente associada ao UX Writing da página. O risco associado é muito baixo, sendo um texto informativo e persuasivo que não sofre na questão de conteúdo, apenas da forma. O texto da tela A ressalta um pouco mais o ponto do desenvolvimento e aprendizado, como se esses fossem fatores propostos pelo acompanhamento dos professores, dando uma maior impressão que o aluno de fato irá se desenvolver durante esse acompanhamento. Essa alteração pode diminuir a persuasão de inscrição ao curso, contudo, seu risco é baixíssimo, visto que a mudança no texto é pouca e a massividade de outros textos informativos presentes na página. O impacto previsto também seria baixo.


## Estratégias para Mitigar ou Lidar com os Riscos Identificados

&emsp;&emsp; Como explicado na seção "Objetivo", os riscos estão diretamente associados à prática do teste A/B, especialmente os testes A/Bs multivariados (cenário do atual projeto, em que estamos testando cinco telas Bs). Existem algumas formas de mitigar os riscos, mas nunca exclui-los totalmente.

### Dados, Propostas Feitas a Partir de Testes

A primeira estratégia é o forte embasamento das hipóteses desenvolvidas, caso nossas sugestões fossem aleatórias ou puramente intuitivas, o risco de termos resultados negativos seria muito maior, assim, todas as mudanças propostas foram construídas a partir de hipóteses desenvolvidas por meio de testes qualitativos. Assim, utilizamos os dados coletados para construir a proposta da tela B.

### Controle do Número de Telas B

A segunda forma de mitigar os riscos associados à implementação da tela B é limitar o número de usuários expostos a ela inicialmente. Isso nos permite avaliar seu impacto em um grupo menor e realizar ajustes antes de uma implementação em escala. De forma geral, recomenda-se que 60% das telas sejam destinadas à tela A e 40% à tela B. Em nosso projeto, essa porcentagem é ainda mais controlada, 94% destinado à tela A e 6% destinados à tela B, uma redução de cerca de 10 vezes do recomendado. Esse alto controle diminui de forma drástica as consequências e riscos associados à implementação das novas telas.


### Mudança Gradual, Limitação de Riscos

A terceira forma de mitigar é evitar mudanças drásticas na página. Além de ser difícil identificar quais fatores contribuíram para o sucesso ou falha da página, manter outros aspectos do site inalterados garante que o nível de sucesso permanecerá semelhante às propostas anteriores, que ainda mantêm várias características das outras páginas. Assim, a variação de resultados não será tão grande, algo que não passa ou diminui dos 10%. Esse é um bom número que permite trabalhar sem tanto receio de comprometer ou perder os resultados alcançados até o momento.










