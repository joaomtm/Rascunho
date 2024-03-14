# Análise Heurística

## Metodologia, Heurísticas Utilizadas

  Para a seguinte análise heurística, serão utilizadas as Heurísticas de Nielsen, mais especificamente, as 10 Heurísticas de Usabilidade para Design de Interface de Usuário ("10 Usability Heuristics for User Interface Design"). Essa lista e definição das heurísticas é escrita pelo próprio Jakob Nielsen, sendo constantemente atualizada, disponível em "Nielsen Norman Group" (https://www.nngroup.com/articles/ten-usability-heuristics/).


## 10 Heurísticas de Usabilidade para Design de Interface de Usuário

Em suma, as 10 Heurísticas de Nielsen são regras gerais de usabilidade para o design de interfaces de usuário. Elas são amplamente utilizadas na indústria de design de interfaces de usuário como um guia fundamental para avaliar e melhorar a usabilidade de produtos digitais, tendo relevância contínua no campo do design centrado no usuário.

## 1: Visibilidade do status do sistema

"O design deve sempre manter os usuários informados sobre o que está acontecendo, através de feedback apropriado dentro de um período de tempo razoável."

Essa heurística não é antendida completamente no Dashboard, até pelas ciscurtâncias atuais do projeto. O wireframe não prevê nenhuma forma de espera entre telas ou interações na página, toda ação é respondida de forma automática.

![image](https://github.com/joaomtm/Rascunho/assets/99208815/aacda503-b37a-46a5-b803-88e99d4aa263)

![image](https://github.com/joaomtm/Rascunho/assets/99208815/cbfb331f-3301-4215-8e44-8f5bf6d40fdb)


É observável que não é considerado nenhum tipo de espera na transição de páginas ou na geração de infográficos, o que é justificável pela ordem do desenvolvimento do mockup e wireframe que priorizaram as telas princiais e os gráficos em detrimento dos seus estados intermediários. Além disso, ainda não se sabe o exatamente o tempo necessário para essas telas de transição, todos os dados estão "mockados", ou seja, são dados fictícios que não acessam o banco de dados, gerando uma falsa sensação de rapidez. Contudo, a previsão é que de fato todas essas transições sejam extremamente rápidas por estarmos trabalhando com uma aplicação "One Page", caracterizada pela rapidez com que os usuários podem acessar e consumir o conteúdo. Os dados consumidos também não são complexos, facilitando na rapidez em gerar infográficos. Por fim, esse problema pode ser classificado como menor, o dashboard desenvolvido não possui longos momentos de espera nas suas transições, não afetando quase nada a experiência final do usuário. Uma possível solução é a aplicação de símbolos ou avisos que indicam o carregamento ou transição.

Ainda falando sobre essa primeira heurística, o status do sistema em fases de uso é completamente satisfeita a partir da navbar construída.

![image](https://github.com/joaomtm/Rascunho/assets/99208815/729f74d3-b24d-4f68-944e-4e1b60a02669)

Cada seção da navbar é bem dividida, definindo com exatidão em qual etapa da solução o usuário está inserido, de forma lógica e contínua. Essa divisão fica explícita nos elementos visuais, sendo a página selecionada destacada de azul. 

## 2: Correspondência entre o sistema e o mundo real

"O design deve falar a língua dos usuários. Use palavras, frases e conceitos familiares ao usuário, em vez de jargões internos. Siga as convenções do mundo real, fazendo com que as informações apareçam em uma ordem natural e lógica."


Essa heurística é atendida de forma plena no dahsboard: a linguagem verbal é extremamente clara e adaptada para os profissionais que utilizarão a solução (inicialmente, apenas o CEO da Volkswagen Brasil), utilizando termos e referências diretas ao contexto em que o problema está inserido.

![image](https://github.com/joaomtm/Rascunho/assets/99208815/122e1594-c55e-451a-99c0-40a7aa9ec373)

A linguagem não verbal no dashboard também atende de forma completa a heurística, com símbolos e cores que são de automático entendimento, não deixando dúvidas de nenhuma funcionalidade a que se refere.

![image](https://github.com/joaomtm/Rascunho/assets/99208815/74430f18-cc32-40c5-af32-55373135aaed)

## 3: Controle e liberdade do usuário

"Os usuários geralmente executam ações por engano. Eles precisam de uma “saída de emergência” claramente marcada para abandonar a ação indesejada sem ter que passar por um processo extenso."

Essa heurística é atendida no dashboard, havendo apenas um ponto de atenção. Primeiro, nas páginas principais do dashboard, a navegação pela navbar é rápida e bem visível (está acima da tela e de forma bem grande), assim, caso o usário clique por erro em outra aba, ele consegue facilmente voltar ou selecionar outra.

![image](https://github.com/joaomtm/Rascunho/assets/99208815/41c273ad-2eef-4571-a56c-044aca7c8f52)

Caso o usuário acesse (intencionalmente ou não) a área de perfil, ele também consegue voltar para a página principal de forma rápida e prática, basta clicar no grande botão "Voltar ao Início" que está acompanhado por uma seta (<-), voltando imediatamente para a página inicial.

![image](https://github.com/joaomtm/Rascunho/assets/99208815/0e82cbc9-aa5a-4536-9498-cd8523f3805f)

![image](https://github.com/joaomtm/Rascunho/assets/99208815/acb1a039-a241-44df-bb5b-fb7a74d36f8d)

![image](https://github.com/joaomtm/Rascunho/assets/99208815/43c1d0e4-129d-4591-be5c-afeac1bfbd38)

A mesma solução é aplicada para a página de editar perfil

![image](https://github.com/joaomtm/Rascunho/assets/99208815/75cff22e-84cc-4f2a-83db-38859a8b5dd9)

Em questão da manipulação dos infográficos, o usuário não é penalizado por erros de análise ou "missclicks". Os infográficos gerados no dashboard se modificam rapidamente e podem ser alterados com apenas dois cliques na aba de configurações do gráfico (o menu suspenso).

![image](https://github.com/joaomtm/Rascunho/assets/99208815/a661ffc7-0ca5-4508-8513-80b375484e0a)
![image](https://github.com/joaomtm/Rascunho/assets/99208815/b7c8d216-872d-4197-81ae-9c670b710391)

Como citado no início dessa seção, há apenas um ponto de atenção que não atende a respectiva heurística: não há a opção de desdeslogar a conta durante o uso do dashboard. Por enquanto enquanto, há apenas um usuário previsto (o CEO), contudo é possível que o próprio CEO queira ter dois acessos diferentes ou que o próprio projeto escale para outros tipos de usuário. Esse é um problema menor, que afeta minimamente a experiência do usuário, que será obrigado a reiniciar a página ou excluir a memória do navegador para fazer um novo login. A solução desse problema é simples, bastando a criação de um botão para sair na página principal ou na área de perfil.

![image](https://github.com/joaomtm/Rascunho/assets/99208815/95dc175d-9213-47ef-8c2d-7f14e72c1e0d)


## 4: Consistência e Padrões

"Os usuários não deveriam se perguntar se palavras, situações ou ações diferentes significam a mesma coisa. Siga as convenções da plataforma e do setor."

## 5: Prevenção de Erros

"Boas mensagens de erro são importantes, mas os melhores designs evitam cuidadosamente a ocorrência de problemas. Elimine condições propensas a erros ou verifique-as e apresente aos usuários uma opção de confirmação antes de se comprometerem com a ação."

![image](https://github.com/joaomtm/Rascunho/assets/99208815/9dc62593-7ac9-490b-babd-3016750514c7)

![image](https://github.com/joaomtm/Rascunho/assets/99208815/66a0c963-d991-46a8-bcd4-55eea440f135)

## 6: Reconhecimento em vez de lembrança

"Minimize a carga de memória do usuário tornando visíveis elementos, ações e opções. O usuário não deveria ter que lembrar informações de uma parte da interface para outra. As informações necessárias para usar o design (por exemplo, rótulos de campos ou itens de menu) devem estar visíveis ou facilmente recuperáveis ​​quando necessário."

## 7: Flexibilidade e Eficiência de Uso

"Atalhos – ocultos para usuários novatos – podem acelerar a interação do usuário experiente, para que o design possa atender tanto usuários inexperientes quanto experientes. Permita que os usuários personalizem ações frequentes."

## 8: Design Estético e Minimalista

"As interfaces não devem conter informações irrelevantes ou raramente necessárias. Cada unidade extra de informação numa interface compete com as unidades de informação relevantes e diminui a sua visibilidade relativa."

## 9: Ajude os usuários a reconhecer, diagnosticar e se recuperar de erros

"As mensagens de erro devem ser expressas em linguagem simples (sem códigos de erro), indicar com precisão o problema e sugerir uma solução de forma construtiva."

## 10: Ajuda e Documentação

"É melhor que o sistema não precise de nenhuma explicação adicional. No entanto, pode ser necessário fornecer documentação para ajudar os usuários a compreender como concluir suas tarefas."
































