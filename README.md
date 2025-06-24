# Dashboard de Avaliação Acadêmica CEUB

Este repositório contém o projeto de um dashboard interativo desenvolvido em Power BI, focado na análise e visualização de dados de avaliação acadêmica do CEUB. O objetivo é transformar dados brutos em insights acionáveis para docentes, coordenação da CPA e coordenação de cursos, facilitando a tomada de decisões e a melhoria contínua da qualidade educacional.

## 🚀 Funcionalidades Principais

O dashboard oferece as seguintes funcionalidades:

*   **Análise Abrangente de Avaliações**: Visualizações detalhadas para Avaliação das Disciplinas (MD1), Avaliação do Curso e Infraestrutura (MD2), e Avaliação do Curso por Inteiro (MD3).
*   **Desempenho Docente e Discente**: Análise do Ensino pelo Discente e Alunos Avaliados por Nota Média por MGA.
*   **Comparação Temporal**: Gráficos de linha para comparar o desempenho atual com períodos anteriores e uma linha de meta para acompanhamento.
*   **Filtros Interativos**: Segmentações de dados para `Modalidade`, `Período Letivo`, `Campus`, `Faculdade|Curso`, `Eixo de Formação`, `Instrumento`, `Grupo de Questão`, `Disciplina` e `Docente`, permitindo uma exploração granular dos dados.
*   **Segurança em Nível de Linha (RLS)**: Implementação de RLS para garantir que cada professor visualize apenas os dados relevantes às suas disciplinas.
*   **Análise de Sentimentos e Questões Discursivas**: Proposta de integração de análise de palavras-chave e sentimento para respostas abertas, com visualizações como Nuvem de Palavras e tabelas detalhadas.
*   **Identidade Visual CEUB**: Design alinhado com a identidade visual do CEUB, utilizando cores e elementos gráficos fornecidos.

## 📊 Estrutura do Projeto

O projeto é composto principalmente pelo arquivo `.pbix` do Power BI e por um guia detalhado de implementação. A estrutura de dados é baseada em um arquivo Excel fornecido.

### Arquivos Principais

*   `Dashboard_Avaliacao_CEUB.pbix`: O arquivo principal do Power BI Desktop contendo o modelo de dados, medidas DAX e todas as visualizações.
*   `CEUB_export-data-desafio-pbi.xlsx`: O dataset de origem com os dados de avaliação acadêmica.
*   `powerbi_guide.md`: Um guia detalhado passo a passo para a construção do dashboard, incluindo instruções para importação de dados, criação de medidas DAX, design de visuais e implementação de RLS.
*   `relatorio_powerbi_ceub.md`: Um relatório completo sobre o desenvolvimento do projeto, cobrindo contexto, público-alvo, dados, visuais, análise de dados, objetivos e desafios.
*   `Identidadevisual-CPA.zip`: Arquivos da identidade visual do CEUB para aplicação no dashboard.
*   `printsdopainelatual.zip`: Imagens de referência do painel atual.

## 🛠️ Como Utilizar

Para visualizar e interagir com o dashboard, siga os passos abaixo:

### Pré-requisitos

*   Power BI Desktop instalado.
*   Acesso ao Power BI Service (para publicação e configuração de RLS).

### Configuração Local

1.  **Clone o Repositório**: Faça um clone deste repositório para sua máquina local:
    ```bash
    git clone <URL_DO_SEU_REPOSITORIO>
    ```
2.  **Descompacte os Arquivos**: Descompacte os arquivos `Identidadevisual-CPA.zip` e `printsdopainelatual.zip` nas suas respectivas pastas.
3.  **Abra o Projeto no Power BI Desktop**: Abra o arquivo `Dashboard_Avaliacao_CEUB.pbix` com o Power BI Desktop.
4.  **Atualize os Dados**: Se o arquivo `CEUB_export-data-desafio-pbi.xlsx` for movido, você precisará atualizar a fonte de dados no Power Query Editor.

### Publicação e RLS no Power BI Service

Para publicar o dashboard e configurar a segurança em nível de linha (RLS):

1.  **Publicar no Power BI Service**: No Power BI Desktop, clique em `Publicar` e selecione o workspace desejado.
2.  **Configurar RLS**: No Power BI Service, vá até o conjunto de dados (dataset) do seu relatório, clique em `Segurança` e atribua os usuários às funções RLS (ex: `ProfessorRole`), garantindo que os UPNs correspondam aos dados dos professores.

## 💡 Medidas DAX Essenciais

Algumas das medidas DAX cruciais para o funcionamento do dashboard incluem:

*   `Média da Avaliação`: Calcula a média ponderada das respostas.
*   `Cor Avaliação`: Define as cores dos visuais com base na média da avaliação e metas.
*   `Meta Avaliação`: Linha de referência para a meta de 4.50/5.0.
*   `Nome Usuário Logado`: Utilizada para a implementação do RLS.
*   `Média Avaliação Período Anterior`: Permite a comparação de desempenho com o período anterior.

## 🤝 Contribuição

Sinta-se à vontade para contribuir com melhorias, sugestões ou correções. Para isso, siga os passos:

1.  Faça um fork do repositório.
2.  Crie uma nova branch (`git checkout -b feature/sua-feature`).
3.  Faça suas alterações e commit (`git commit -m 'feat: Adiciona nova funcionalidade'`).
4.  Envie para a branch (`git push origin feature/sua-feature`).
5.  Abra um Pull Request.

## 📄 Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.

## 📞 Contato

Para dúvidas ou sugestões, entre em contato com [Lucas-Wall].

---

