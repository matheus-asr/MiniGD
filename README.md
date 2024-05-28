## Análise de geração e consumo - Mini GD

# Visão geral

Este projeto visa a análise de dados referentes a minigeração distribuída no Brasil, analisando características como crescimento anual, estados contribuintes, consumo, fonte de energia etc. Todos os dados deste estudo são provenientes da Agência Nacional de Energia Elétrica (ANEEL), e são de domínio público. 

O painel de dashboard no PowerBI elaborado pode ser acessado a partir do link: ( https://app.powerbi.com/view?r=eyJrIjoiNDEzZGMwNTktNDI1YS00ZDAxLTkxYTQtYTBhNTc5NzlmNDExIiwidCI6IjJmYTNkYTk2LWVjNjItNGM3MC05MWRjLTMwMDkzYmRiMzdkNiJ9 ) 


# Desenvolvimento

Para o desenvolvimento deste projeto, foram utilizados scripts em Python 3.12 para a API e manipulação de dados, e um dashboard no PowerBI para a visualização destes.
Os dados abertos estão hospedados no sistema de gerenciamento de dados CKAN, e foram obtidos a partir de API's em Python, uma vez que foram utilizados dois conjuntos de dados distintos. Para a análise exploratória, tratamento, e manipulação de dados foram utilizadas as bibliotecas Pandas, JSON, e IO. 

Uma vez prontos, foi feita a exportação de dois scripts em Python para o PowerBI, Historico.ipynb e Empreendimentos.ipynb, que podem ser encontrados neste repositório. A partir desta integração, o PowerBI pode atualizar os dados de forma autônoma. Foi observado, entretanto, oscilações quanto à disponibilidade de acesso ao banco de dados por parte do sistema de gerenciamento de dados. 

Após carregar os dois conjuntos de dados para o PowerBI, foi criada uma tabela Calendário, a partir da linguagem DAX, a fim de gerenciar o relacionamento de datas entre as tabelas Empreendimentos e Historico. Em ambos os casos, foram utilizados relacionamentos de um para muitos, da tabela Calendario para as demais. Posteriormente, foram gerados os gráficos a serem analisados.


# Análises

Os gráficos e indicadores foram elaborados com o objetivo de se analisar a evolução da minigeração distribuída ao longo dos anos, assim como os estados e distribuidoras com maior geração, e o consumo por classe de consumidor desta fatia da geração distribuída. Entre as informações mais relevantes, se encontra o crescimento de aproximadamente 44% da potência instalada anualmente entre 2022 e 2023 na minigeração, indicando o aquecimento do mercado da geração distribuída.
 
Outro fator a ser destacado neste mesmo período é o crescimento do consumo comercial, em contraste com a redução do consumo residencial. Com a diminuição de custos de painéis solares, comércios que dispõem de uma grande área útil para a implementação destas, como em telhados e estacionamentos, têm investido na geração distribuída para a redução de custos quanto ao consumo de energia. Isso também pode ser observado ao comparar a geração de energia para autoconsumo local com as demais modalidades de consumo. Entretanto, deve-se observar ainda que este estudo se refere somente à minigeração, e para consumo residencial, o consumidor tende a investir em empreendimentos menores, caracterizados como microgeração.

A partir da análise dos gráficos nota-se também que os estados do sudeste lideram entre os maiores geradores, principalmente os estados de Minas Gerais e São Paulo, impulsionados por incentivos fiscais por parte dos governos estaduais. O grande número de usinas instaladas e unidades consumidoras, entretanto, pode gerar saturação do mercado nestes estados, fazendo com que seja vantajoso o investimento em mercados ainda em ascensão.

Após a conclusão do projeto observa-se a necessidade de um aprofundamento nas particularidades do mercado energético que podem gerar tendências, como incentivos tributários de cada estado, tarifas energéticas, variação de custos de equipamentos utilizados na geração distribuída, entre outros. Para uma análise completa do cenário de geração distribuída, também se faz necessária a inclusão de dados referentes à microgeração, que representa uma grande, e ainda crescente parcela sobre a capacidade de geração nacional.


# Referências

Os dados abertos utilizados estão disponíveis para consulta através do link: ( https://dadosabertos.aneel.gov.br/organization/agencia-nacional-de-energia-eletrica ). <Acesso em 27 de maio de 2024.>

