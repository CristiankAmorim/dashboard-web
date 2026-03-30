# 🖥 SGF — Dashboard de Fiscalização de Obras
 
 Sistema de Gestão Financeira para acompanhamento e controle de obras, com visualização integrada de planilhas e análise de Curva ABC.


 ## 🗂️ Sobre o Projeto
 
O **SGF (Sistema de Gestão Financeira)** é um dashboard web desenvolvido para auxiliar na fiscalização e controle financeiro de obras. Ele centraliza informações relevantes da obra em uma interface simples e acessível, consumindo dados diretamente de uma planilha do Google Sheets publicada na web.
 
O sistema permite o acompanhamento em tempo real das informações financeiras, incluindo:
 
- Controle de custos e despesas da obra;
- Visualização de itens por categoria e valor;
- **Análise da Curva ABC**, permitindo a classificação dos insumos/serviços por impacto financeiro;
- Dados sempre atualizados via integração com Google Sheets.


## ⚙ Funcionalidades
 
- ✅ Exibição de planilha com dados financeiros da obra em tempo real;
- ✅ Integração direta com Google Sheets (sem necessidade de backend);
- ✅ Gráfico e tabela de **Curva ABC** para análise de insumos e serviços;
- ✅ Interface responsiva e de fácil leitura.


## ♨ Tecnologias Utilizadas
 
| Tecnologia | Uso |
|---|---|
| HTML5 | Estrutura da página |
| CSS3 | Estilização e layout |
| JavaScript | Lógica de carregamento dinâmico |
| Google Sheets | Fonte de dados (planilha publicada) |


## 🔗 Configurando a Planilha
 
Para apontar o dashboard para uma planilha diferente:
 
1. No Google Sheets, vá em **Arquivo → Compartilhar → Publicar na web**
2. Selecione a aba desejada e o formato **Página da Web**
3. Copie o link gerado
4. No `index.html`, substitua a variável `base` pela nova URL:
 
```javascript
const base = "SUA_URL_AQUI";
```

⚠️ A planilha é carregada via `iframe` a partir de uma URL pública do Google Sheets. Certifique-se de que a planilha está publicada na web para que os dados sejam exibidos corretamente.


## 📈 Curva ABC
 
A Curva ABC é uma ferramenta de análise de gestão que classifica os itens de uma obra em três grupos conforme seu impacto financeiro:
 
| Classe | Representação | Impacto Financeiro |
|---|---|---|
| **A** | ~20% dos itens | ~80% do custo total |
| **B** | ~30% dos itens | ~15% do custo total |
| **C** | ~50% dos itens | ~5% do custo total |
 
Essa análise permite priorizar o controle e a fiscalização dos itens de maior valor, otimizando a gestão da obra.
