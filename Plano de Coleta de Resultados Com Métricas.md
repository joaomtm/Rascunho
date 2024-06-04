# Plano de Coleta de Resultados Com Métricas

## Objetivo 

&emsp;&emsp; Este segmento da documentação tem como objetivo detalhar o plano proposto para a coleta de resultados do teste A/B. Quando as telas Bs forem aplicadas no site da Wizard On, diversos dados serão gerados e armazenados. Contudo, é crucial definir quais desses dados de fato representam boas métricas para avaliarmos o desempenho das novas telas propostas. Assim, será desenvolvido um plano para uma minuciosa coleta de resultados que futuramente permitirá uma análise preliminar dessa apuração.


## Fonte Inicial de Dados, Looker Studio Google

&emsp;&emsp; O Looker Studio é uma ferramenta de visualização de dados e criação de relatórios interativos oferecida pelo Google. Para este projeto, a Pearson configurou diretamente o Looker para acessar os dados coletados atualmente pelos endereços de site referentes à Wizard On. Para esta análise preliminar e para o primeiro plano de coleta de resultados, apenas essa fonte primária do Looker será considerada.

<p align="center">
  <img src="https://github.com/joaomtm/Rascunho/assets/99208815/9a79aba1-e097-410e-ae11-f38cbede1b40" alt="image">
</p>

> Looker Studio Google (Logo)


![image](https://github.com/joaomtm/Rascunho/assets/99208815/e1639553-bbcd-457e-bb26-d71c9ad7c49f)

> Página Inicial do Looker construído pela Pearson

&emsp;&emsp; O Looker desenvolvido organiza os endereços dos sites de duas maneiras: algumas seções agrupam todos os sites relacionados à Wizard On (ex: "Big Picture"), enquanto outra seções segmentam cada URL individualmente. Para comparar efetivamente os resultados das variantes A e Bs das páginas, devemos focar nas seções “Acessos” e “Eventos”. Estas seções nos permitem filtrar pelo “Page Path” (Endereço da Página), recurso essencial para nossa comparação e análise.

![image](https://github.com/joaomtm/Rascunho/assets/99208815/3fc103d3-057f-4f7b-999a-ee98035d0b5a)

> Página "Acessos" do Looker


![image](https://github.com/joaomtm/Rascunho/assets/99208815/89092742-9738-4a0c-8f64-39ed422c72e9)

> Página "Eventos" do Looker

## Matriz Heart + GSM

&emsp;&emsp; Tendo seu primeiro desenvolvimento na Sprint 1, a Matriz Heart é uma ferramenta utilizada para avaliar e medir a satisfação e o engajamento dos clientes com base em cinco aspectos principais: Happiness (Felicidade), Engagement (Engajamento), Adoption (Adoção), Retention (Retenção) e Task Success (Sucesso nas Tarefas). A partir dessas métricas de sucesso, podemos avaliar o desempenho de cada tela e compará-las entre si. Agora, com o objetivo de aplicar diretamente a Matriz Heart ao projeto, será feito um paralelo das métricas presentes no Looker com as métricas previstas na Matriz. Contudo, já é previsto que nem todas as métricas sejam contempladas no Looker, reservando espaço para dar continuidade a essa análise na Sprint 5, momento em que serão disponibilizados mais dados e com mais detalhes.

![image](https://github.com/joaomtm/Rascunho/assets/99208815/d6d10b5e-c0a6-46c2-bea7-b100be098fa5)

> Matriz Heart

Link para documentação da Matriz Heart: https://github.com/Inteli-College/2024-1B-T04-SI10-G02/blob/main/document/Sprint%2001/HEART.md


## Plano de Coleta, Seleção de Métricas

&emsp;&emsp; Na seção "Acessos" cinco métricas úteis para análise foram identificadas: Sessions (Seções), Conversions (Conversões), Active Users (Usuários Ativos), a razão de Seções por Usuários Ativos e a razão de Seções por Conversões. A partir dessas métricas, podemos identificar:
- Quantos usuários exatamente utilizaram cada página do teste A/B (Seções)
- Quantos deles se increveram no curso (Conversões)
- Quantos interagiram com a página (Usuários Ativos)
- Porcentagem de usuários que entraram no página e interagiram com ela (Seções/Usuários Ativos)
- Porcentagem de usuários convertidos (Seções/Conversões)

As métricas Usuário Ativos e Seções/Usuários Ativos podem ser relacionado ao **Engajamento** ("M2: Número de interações com elementos interativos na página."). Usuários ativos e a razão de seções por usuários ativos medem quantos usuários interagiram com a página, fornecendo uma visão clara do engajamento do público.

A métrica Seções/Conversões pode ser relacionado a **Adoção** ("M1: Número de formulários de inscrição enviados.") e **Task Success** ("M1: Taxa de inscrição completa sem assistência."). A razão de seções por conversões mostra a eficácia da página em converter visitas em ações concretas, refletindo tanto a adoção do serviço quanto o sucesso em completar tarefas.


![image](https://github.com/joaomtm/Rascunho/assets/99208815/f70d2b3a-b935-480e-8335-7b949b0af037)

> Página "Acessos" do Looker


&emsp;&emsp; Na seção "Eventos", as seguintes métricas foram identificadas: page_view (Vizualização da Página), session_start (início de Sessão), interaction (Interação), user_engagement (Engajamento do Usuário), scroll, click e Click-WhatsApp. A partir dessas métricas será possível identificar:

- Porcentagem e número de pessoas que vizualizaram a página (page_view)
- Porcentagem e número de pessoas que começaram a interagir com a página (session_start e interaction)
- Porcentagem e número de usuários que interagiram de forma engajada com a página (user_engagement)
- Porcentagem e número de usuários que "scrolaram" a página (scroll)
- Porcentagem e número de usuários que clicaram em algum botão da página (click)
- Porcentagem e número de usuários que clicaram no botão Whatssap (Click-WhatsApp)

As métricas page_view, session_start, interaction, user_engagement e click podem ser relacionado ao **Engajamento** ("M2: Número de interações com elementos interativos na página."). Essas métricas indicam o nível de interação do usuário com a página, mostrando quantas pessoas visualizaram, iniciaram sessões, interagiram e clicaram em elementos, refletindo o engajamento geral.

A métrica scroll pode ser relacionado à **Task Sucess** ("M1: Taxa de inscrição completa sem assistência"). O scroll demonstra que os usuários estão explorando a página completamente, indicando uma busca por informações extras ou ajuda.

A métrica Click-WhatsApp pode ser relaciona à **Adoção** ("M1: Número de formulários de inscrição enviados."). O clique no botão WhatsApp indica que os usuários estão tomando medidas para se comunicar ou se inscrever, refletindo a adoção do serviço oferecido.






















