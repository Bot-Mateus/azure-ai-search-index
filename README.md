# Solução de Mineração de Conhecimento com Azure AI Search index

Este repositório contém documentação sobre a configuração e uso de um índice de pesquisa Azure AI usando como exemplo a Fourth Coffee, uma rede nacional de cafeterias, para analisar as experiências dos clientes.
Tentei resumir os passos de criação e dar outros exemplos de utilidade para esses recursos, espero que o material os ajude de algum jeito.

# Índice

- [Visão Geral](#visão-geral)
- [Recursos Azure Necessários](#recursos-azure-necessários)
- [Instruções](#instruções)
  - [Criar Recurso Azure AI Search](#criar-recurso-azure-ai-search)
  - [Criar Recurso Azure AI Services](#criar-recurso-azure-ai-services)
  - [Criar uma Conta de Armazenamento](#criar-uma-conta-de-armazenamento)
  - [Carregar Documentos no Armazenamento Azure](#carregar-documentos-no-armazenamento-azure)
  - [Indexar os Documentos](#indexar-os-documentos)
  - [Consultar o Índice](#consultar-o-índice)
  - [Revisar o Knowledge Store](#revisar-o-knowledge-store)
 - [Outras Aplicações para Recursos Azure](#outras-aplicações-para-recursos-azure)
- [Ferramentas e Tecnologias Beneficiadas](#ferramentas-e-tecnologias-beneficiadas)
- [Aprendizados Adquiridos](#aprendizados-adquiridos)
- [IMPORTANTE: Limpeza](#importante-limpeza)
- [Como me encontrar](#como-me-encontrar)

## Visão Geral

A Fourth Coffee tem como objetivo construir uma solução de mineração de conhecimento para buscar insights sobre as experiências dos clientes. Isso envolve a criação de um índice de pesquisa Azure AI usando dados extraídos de avaliações de clientes. Neste laboratório, você irá:

-   Criar recursos Azure
-   Extrair dados de uma fonte de dados
-   Enriquecer dados com habilidades de IA
-   Usar o indexador da Azure no portal Azure
-   Consultar seu índice de pesquisa
-   Revisar resultados salvos em um Knowledge Store

## Recursos Azure Necessários

Os seguintes recursos Azure são necessários para esta solução:

-   Recurso Azure AI Search
-   Recurso Azure AI services
-   Conta de armazenamento com containers de blob

## Instruções

### Criar Recurso Azure AI Search

1.  Faça login no portal Azure.
2.  Clique no botão + Criar um recurso e pesquise por Azure AI Search.
3.  Crie um recurso Azure AI Search com as configurações especificadas.
4.  Após a implantação, acesse o recurso para gerenciar índices e pesquisa.

### Criar Recurso Azure AI Services

1.  Volte para a página inicial do portal Azure.
2.  Clique no botão + Criar um recurso e pesquise por Azure AI services.
3.  Configure o recurso Azure AI services com as configurações especificadas.
4.  Após a implantação, visualize os detalhes da implantação.

### Criar uma Conta de Armazenamento

1.  Volte para a página inicial do portal Azure.
2.  Selecione o botão + Criar um recurso e pesquise por uma conta de armazenamento.
3.  Crie um recurso de Conta de Armazenamento com as configurações especificadas.
4.  Habilite o acesso anônimo aos blobs na configuração.

### Carregar Documentos no Armazenamento Azure

1.  Crie um container na conta de armazenamento.
2.  Baixe e extraia as avaliações de café fornecidas no link [zipped coffee reviews](https://aka.ms/mslearn-coffee-reviews).
3.  Faça o upload dos arquivos extraídos para o container.

### Indexar os Documentos

1.  Navegue até o seu recurso Azure AI Search.
2.  Use o Assistente de Importação de dados para criar um índice e importar documentos do armazenamento.
3.  Configure os detalhes da fonte de dados e habilidades cognitivas.
4.  Personalize o índice de destino e crie um indexador.
5.  Aguarde a conclusão da indexação.

### Consultar o Índice

1.  Use o Explorador de Pesquisa no portal Azure para escrever e testar consultas.
2.  Escreva consultas para filtrar resultados por localização e sentimento.
3.  Revise os resultados da pesquisa e sua relevância.

### Revisar o Knowledge Store

1.  Navegue até a sua conta de armazenamento Azure.
2.  Explore o conteúdo do container do Knowledge Store.
3.  Veja os arquivos JSON contendo dados enriquecidos extraídos das avaliações.
4.  Explore arquivos de imagem e tabelas contendo frases-chave extraídas pelo conjunto de habilidades.

## Outras Aplicações para Recursos Azure

Além da utilização para análise de experiências de clientes, os recursos Azure abordados neste projeto têm uma ampla gama de aplicações em diversos setores e cenários. Algumas delas incluem:

-   **Análise de Sentimento em Mídias Sociais**: Empresas podem utilizar recursos de análise de sentimentos para entender a percepção do público sobre seus produtos, serviços ou marca nas mídias sociais. Isso permite identificar tendências, problemas emergentes e oportunidades de engajamento.
    
-   **Pesquisa e Análise de Dados Científicos**: Pesquisadores e cientistas podem utilizar recursos de pesquisa para indexar grandes conjuntos de dados científicos, facilitando a descoberta de padrões, tendências e insights em áreas como biologia, genômica, medicina e ciências ambientais.
    
-   **Apoio à Decisão em Saúde**: Hospitais e instituições de saúde podem implementar sistemas de busca e análise para ajudar os profissionais de saúde a acessar rapidamente informações relevantes sobre diagnósticos, tratamentos e melhores práticas, contribuindo para decisões clínicas mais informadas e eficazes.
    

## Ferramentas e Tecnologias Beneficiadas

As soluções Azure AI Search e Azure AI Services podem ser integradas a uma variedade de ferramentas e tecnologias para melhorar seus recursos e funcionalidades. Algumas delas incluem:

-   **Microsoft Power BI**: Integração com o Power BI permite a criação de painéis interativos e visualizações de dados alimentados diretamente pelo índice de pesquisa, fornecendo insights acionáveis de maneira acessível e intuitiva.
    
-   **Microsoft Dynamics 365**: Integração com o Dynamics 365 permite aprimorar a inteligência do cliente e a automação de vendas, utilizando dados enriquecidos por habilidades de IA para personalizar interações e otimizar processos de negócios.
    
-   **Ferramentas de Desenvolvimento Personalizadas**: Desenvolvedores podem aproveitar as APIs e SDKs fornecidos pela Azure para criar aplicativos personalizados e soluções específicas para suas necessidades, aproveitando os recursos de pesquisa e IA de forma flexível e adaptável.
    

## Aprendizados Adquiridos

Durante o processo de configuração e uso dos recursos Azure para a Fourth Coffee, alguns aprendizados importantes foram adquiridos:

-   **Importância da Integração de Recursos**: Integrar recursos como Azure AI Search, Azure AI Services e armazenamento de dados é essencial para criar uma solução robusta e eficaz.
    
-   **Necessidade de Personalização e Ajuste Fino**: A capacidade de personalizar e ajustar parâmetros, como habilidades cognitivas e configurações de indexação, é crucial para garantir que a solução atenda às necessidades específicas do negócio e forneça resultados relevantes e precisos.
    
-   **Monitoramento e Manutenção Contínuos**: Após a implantação da solução, é importante monitorar continuamente o desempenho do índice de pesquisa, avaliar a qualidade dos resultados e realizar ajustes conforme necessário para garantir a eficácia e relevância contínuas da solução.

# IMPORTANTE: Limpeza

Se você não pretende fazer mais exercícios, exclua quaisquer recursos que não precise mais para evitar custos desnecessários.

Saiba mais: [Página do Azure AI Search index (UI)](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Labs/11-ai-search.html)

# Como me encontrar

<p align="left">
<!-- <a href="https://elbrusagency.com/"><img src="https://img.shields.io/badge/-elbrusagency.com-3423A6?style=flat&logo=Google-Chrome&logoColor=white"/></a> -->
<a href="https://www.linkedin.com/in/mateus-carvalho-da-silva/"><img src="https://img.shields.io/badge/-Mateus%20Carvalho-0077B5?style=flat&logo=Linkedin&logoColor=white"/></a>
<a href="mailto:carvalho.silva2001@gmail.com"><img src="https://img.shields.io/badge/-carvalho.silva2001@gmail.com-D14836?style=flat&logo=Gmail&logoColor=white"/></a>
<a href="https://www.instagram.com/mateusoaksilva/"><img src="https://img.shields.io/badge/-@mateusoaksilva-E4405F?style=flat&logo=Instagram&logoColor=white"/></a>
</p>
