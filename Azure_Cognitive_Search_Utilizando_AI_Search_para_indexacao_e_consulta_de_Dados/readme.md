# Soluções de Pesquisa Cognitiva do Azure
## Enriquecimento e Índice de IA
- Permite uma compreensão mais profunda dos dados com uso de IA.
- Utiliza visão computacional, processamento de linguagem natural, etc.
- A indexação transforma o conteúdo em algo pesquisável.
## Ingestão de Dados
- Azure Blob Storage containers: Armazenamento de grandes volumes de dados não estruturados.
- Azure Data Lake Storage Gen2: Armazenamento otimizado para análise de dados em larga escala.
- Azure Table Storage: Armazenamento NoSQL para dados estruturados.
## Explorar
- Pesquisa realizada sobre os índices gerados.
- Integração dentro de aplicativos para busca inteligente.
- Possibilidade de criar visualizações de dados com os resultados.
## O que é Mineração de Conhecimento?
- Azure Cognitive Search é a plataforma de mineração de conhecimento alimentada por IA do Azure.
## Enriquecimento de IA (Parte 1)
- Reconhecimento de entidades no texto.
- Tradução automática de conteúdo.
- Avaliação de sentimentos presentes nos textos.
## Enriquecimento de IA (Parte 2)
- Documentos enriquecidos são produzidos por habilidades de IA.
- Esses dados são consumidos durante a indexação.
- Dados serializados são enviados ao mecanismo de pesquisa para indexação.
## Pratica
- Situação problema: Uma empresa de cafe no Brasil quer saber como esta a satisfação dos clientes em relação ao seus produtos.
- Para a resolução do problema vamos usar uma serie de recursos:
  - Azure AI services | AI Search
    - Depois de entrar na plataforma criamos um novo AI services com um nome especifico para ele, escolhemos a linha BASIC de servilos com apenas 2GB, seleciona o tipo e a localização(não recomendado por no Brasil por questão de custo) e então ja podemos criar.
  - Recurso de AI
    - Vai em criar novo recurso, em categorias vai em AI + Machine Learning e então no Azure AI services clica em create
    - Selecionamos a subinscrição correspondente com o resource group, seleciona a região(não recomendado por no Brasil por questão de custo), criamos um nome especifico para ele, escolhemos o Standart S0, selecionamos o checkbox e então ja podemos criar.
  - Conta de armazenamento
    - Na Home selecionamos a opção Storage accounts -> Criar, aqui temos muitas opções mas para selecionar o problema da nossa situação deste laboratorio ja inserimos as informações de assinatura e o mesmo resource group que estão os dois anteriores, criamos um nome especifico para ele de 3 a 24 caracteres, seleciona a região(não recomendado por no Brasil por questão de custo),em performance selecionamos a standard, em redundancy selecionamos o (LRS) e então review e create.
    - Nele podemos armazenar dados como containers, arquivos, tabelas, varios tipos de recursos, mas nos temos que determinar isso atravez das configurações (para o laboratorio deixamos desabilitado o Allow Blob anonymous acces).
    - Depois criamos um novo container e mandamos os arquivos(no laboratorio os arquivos com as simulações das revisões dos usuarios)
  - No mecanismo de busca(AI Search) eu importo o local a onde estao os dados para que funcione como consuta ao banco de dados que posso estar sempre consutando