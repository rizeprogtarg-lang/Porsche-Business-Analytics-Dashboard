# Porsche Brasil | Business Analytics & Sales Intelligence 🏎️📊

Este projeto é um dashboard interativo de vendas desenvolvido num único ficheiro HTML[cite: 4]. Foi desenhado para analisar 100 registos de vendas sanitizadas de veículos da Porsche[cite: 4], transformando dados brutos em inteligência de negócio navegável através de uma interface executiva e refinada, inspirada no design da marca (Dark Mode, Tailwind CSS, Chart.js)[cite: 4].

🔗 **[Aceda ao Dashboard Publicado Aqui](https://SEU-USUARIO-AQUI.github.io/NOME-DO-REPOSITORIO/)** *(Substitua este link pelo endereço real do seu GitHub Pages)*

## 🎯 Perguntas de Negócio Escolhidas
Para garantir que o dashboard entregava valor real e não apenas gráficos avulsos, foquei-me em três questões fundamentais para a estratégia comercial de concessionárias de luxo:

1. **Quais os principais modelos de carro vendidos por cidade?**
   - **Porquê:** O painel "Ranking Regional" cruza as praças geográficas com o modelo "Campeão" local. Isto permite aos gestores entenderem as preferências regionais (ex: SUVs no interior vs. Desportivos no litoral) e otimizarem a alocação de stock e logística de entrega[cite: 4].
2. **Qual o ano de modelo de carro (Model Year) com maior saída?**
   - **Porquê:** A secção "Ciclo Model Year (MY)" responde a isto, isolando o ano de 2024 como o pico histórico de vendas[cite: 4]. É crucial entender se o cliente de luxo prioriza exclusivamente os lançamentos atuais ou se há um mercado secundário forte de modelos anteriores.
3. **Quais os insights dinâmicos sobre popularidade de vendas e pagamentos em cada cidade?**
   - **Porquê:** Em vez de gráficos estáticos, foi implementado um "Insight Engine Dinâmico"[cite: 4]. Ao cruzar filtros de Cidade e Família de Veículo, o sistema recalcula em tempo real a percentagem de adoção de elétricos/híbridos e os métodos de pagamento mais fortes (ex: *Wire Transfer* vs *Financing*)[cite: 4]. Isto estrutura estratégias de parcerias com bancos locais.

## 🤖 O Prompt Utilizado e a Evolução
O desenvolvimento começou com o seguinte prompt inicial entregue a um LLM:

> "Atua como um engenheiro de software e analista de dados sénior. Tenho uma base de dados em formato JSON com 100 vendas sanitizadas da Porsche. Cria um dashboard num ficheiro único em HTML que não necessite de servidor. O visual deve ter um aspeto executivo, luxuoso e refinado, utilizando Tailwind CSS (Dark Mode com detalhes em vermelho e dourado) e Chart.js. Inclui KPIs de topo, 4 filtros principais (Modelo, Ano, Cidade, Pagamento) e desenvolve painéis que respondam às seguintes perguntas: Principais modelos por cidade, ano mais vendido e uma área de insights dinâmicos. Adiciona também uma tabela de dados pesquisável."

**O que mudou até à versão final:**
A evolução principal ocorreu na substituição de relatórios cruzados estáticos por uma arquitetura reativa em JavaScript[cite: 4]. Foi adicionado um sistema de *Tabs* por "Família de Veículo" (911, Macan, Taycan, etc.)[cite: 4], uma tabela com paginação inteligente e um botão funcional para exportação dos dados filtrados para CSV, garantindo autonomia analítica ao utilizador final[cite: 4].

## 🧹 Tratamento Prévio da Base de Dados
Antes da injeção no código HTML, a base de dados original em Excel passou por um processo de sanitização:
- Isolou-se exclusivamente a aba "Sanitized", descartando dados não tratados.
- As colunas de Faturamento (`SalesPriceSanitized`) foram convertidas rigorosamente para formato numérico (float)[cite: 4], removendo formatações de texto/moeda que impediriam os cálculos de Ticket Médio e Receita Total no JavaScript[cite: 4].
- A base final foi exportada em formato JSON otimizado (`orient='records'`) e embutida de forma estática na variável `porscheData` diretamente no `<script>` do ficheiro HTML[cite: 4].

## 🛠️ Tecnologias e Ferramentas
- **Frontend:** HTML5, JavaScript Vanilla, Tailwind CSS (via CDN) e FontAwesome[cite: 4].
- **Visualização de Dados:** Chart.js para os gráficos (Barras, Linhas de Tendência e Doughnut)[cite: 4].
- **IA/Agente:** O fluxo de construção foi suportado por Inteligência Artificial Generativa para arquitetar a lógica de agregação em tempo real (`reduce`, `filter`, `map` no JavaScript) e moldar o design UI/UX de alta fidelidade sem a necessidade de frameworks complexos como React ou Angular[cite: 4].

## 🚀 Como Executar
1. Aceda ao link da aplicação no GitHub Pages.
2. Utilize a barra superior ou as secções laterais para interagir com os **Filtros**.
3. Verifique os painéis de perguntas de negócio e os gráficos a recalcularem as informações instantaneamente[cite: 4].
4. Para testar o ambiente de forma local, basta descarregar o ficheiro `index.html` e abri-lo em qualquer navegador de internet moderno (Google Chrome, Edge, Safari).
