# FURB - Pós Data Science - Trabalho final de ChatBots
## Introdução
Este documento trata-se do desenvolvimento de um trabalho final da disciplina de ChatBots da [Pós Graduação em Data Science da FURB](https://www.furb.br/web/5435/cursos/especializacao/cursos/cursos-em-andamento/data-science), solicitado pelo professor [Cristiano Roberto Franco](https://www.linkedin.com/in/crfranco/).
O chatbot foi desenvolvido utilizando tecnologias de inteligência artificial do [IBM Watson](https://www.ibm.com/br-pt/watson), o qual aplica técnicas de entendimento de linguagem natural (NLU- Natural Language Understanding).
Para acessar e interagir com chatbot desenvolvido para o trabalho, basta acessar o site: [www.kerubin.com.br](https://www.kerubin.com.br). Na base da página do site, no canto direito, clique no ícone: ![Icone do chatebot](https://github.com/lobokoch/chatbot/blob/main/chatbot_icone.png?raw=true). Funciona também para dispositivos móveis como celulares.

## Funcionamento
O chat inícia se apresentado ao usuário e solicitando o seu nome para inciair o atendimento.
Basicamente o ChatBot oferece três tipos de auxílio ao usuário:
- **Consultar fatura de luz (SC)**
   - Fornecido um CPF e uma data de nascimento, o Bot busca a data de vencimento e o valor da primeira fatura de luz em aberto na [Celesc de SC](https://agenciaweb.celesc.com.br/AgenciaWeb/autenticar/loginUC.do). Caso não encontre nenhuma fatura em aberto, indica que não há débitos.
- **Consultar fatura de água (Samae Blumenau)**
    - Fornecido um número de matrícula da Samae de Blumenau (formato numérico), o Bot busca o valor em aberto daquela matrícula junto ao [Samae de Blumenau](http://189.125.181.209:8081/gsan/exibirEmitirSegundaViaContaInternetAcessoGeralAction.do?acessoGeral=sim). Caso não encontre nenhuma fatura em aberto, indica que não há débitos.
- **Pesquisar um endereço pelo CEP**
     - Fornecido um CEP, o Bot busca o endereço do CEP informado chamando a API do [ViaCEP](https://viacep.com.br/).

A qualquer momento, após o Bot ter dado uma resposta, o usuário pode digitar **tchau** indicando ao Bot que quer abandonar o atendimento. Neste caso o Bot se despede e reinicia o atendimento.

## Fluxograma do funcionanemto
Abaixo segue o fluxograma detalhado do funcionamento do ChatBot:
![Fluxograma do chatebot](https://github.com/lobokoch/chatbot/blob/main/chatbot_fluxo.png?raw=true)

## Fonte do projeto no Watson
Clicando [aqui](https://raw.githubusercontent.com/lobokoch/chatbot/main/skill_chatbot.json) é possível visualizar o JSON da Skill do ChatBot no Watson da IBM.

## Estatísitcas com indicadores e métricas
A seguir são apresentados alguns indicadores e métricas das conversas com o ChatBot no período de 10/05/2021 até 14/05/2021.

- **Total de conversas: 55**
- **Média de mensagens por conversa: 5,04**
- **Maior conversa (em número de mensagens): 33**
- **Quantidade de mensagens mal entendidas pelo Bot: 50**

Seguem alguns gráficos estatísitcos fornecidos pelo painel de gerenciamento do IBM Watson Assistent:

**Total de cobertura no entendimento das mensgaens:**
![grafico](https://raw.githubusercontent.com/lobokoch/chatbot/main/grafico_average.png)

**Total de conversas no período:**
![grafico](https://raw.githubusercontent.com/lobokoch/chatbot/main/grafico_total_conversations.png)

**Média de mensagens por conversa (esquerda) e total de mensagens (direita):**
![grafico](https://raw.githubusercontent.com/lobokoch/chatbot/main/grafico_avg_and_total_messages.png)

**Total de usuários atívos (esquerda) e média de conversas por usuário (direita):**
![grafico](https://raw.githubusercontent.com/lobokoch/chatbot/main/grafico_active_users_and_avg_conversa_user.png)

## Considereções finais
Desenvolver um ChatBot utilizando tecnologias de inteligência artificial como o IBM Watson, o qual aplica técnicas de entendimento de linguagem natural (NLU- Natural Language Understanding), é muito produtivo, relativamente simples e muito fácil de integrar com aplicativos e API externas utilizando Webhooks, os quais podem chamar as IBM functions ou AWS Lambdas, onde é possível orquestrar chamadas, em Python por exemplo, para qualquer outro sistema ou API externa com extrema facilidade.
