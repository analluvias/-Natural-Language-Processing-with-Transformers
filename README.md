# Natural Language Processing with Transformers

Este repositório contém os exercícios do livro Natural Language Processing with Transformers: Building Language Applications with Hugging Face. O objetivo é documentar meu progresso e compartilhar os exercícios propostos, trazendo explicações do próprio livro com algumas anotações extras quando considerado necessário.

## Capítulo 1: Hello Transformers

*   **Hello Transformers**: **Apresentação dos Transformers** como uma revolução no mundo do NLP, superando as Redes Neurais Recorrentes (**RNNs**) em tarefas como tradução automática.
*   **The Encoder-Decoder Framework**: Explicação da **estrutura básica dos Transformers**, composta por um **codificador** para processar a entrada e um **decodificador** para gerar a saída, ideal para tarefas de **sequência para sequência**.
*   **Attention Mechanisms**: Destaque da importância dos **mecanismos de atenção**, que permitem ao modelo **focar nas partes relevantes da sequência de entrada** ao gerar a saída, superando o gargalo de informação do último estado oculto em modelos recorrentes.
*   **Transfer Learning in NLP**: Introdução ao uso do **aprendizado de transferência** em NLP, onde modelos **pré-treinados** em grandes corpora podem ser **ajustados finamente** para tarefas específicas com menos dados rotulados, marcando uma mudança significativa em relação ao treinamento do zero.
*   **Hugging Face Transformers**: Apresentação da biblioteca **Hugging Face Transformers** como uma ferramenta fundamental para **facilitar o desenvolvimento de NLP** ao fornecer uma interface unificada para diversos modelos Transformer e ferramentas para treinamento e implantação.
*   **A Tour of Transformer Applications**: Visão geral das diversas **aplicações dos Transformers**:
    *   **Classificação de Texto**: Determinar a categoria ou sentimento de um texto.
    *   **Reconhecimento de Entidades Nomeadas**: Identificar entidades como pessoas, organizações e locais em um texto.
    *   **Resposta a Perguntas**: Extrair a resposta para uma pergunta a partir de um texto.
    *   **Resumo**: Gerar uma versão concisa de um texto mais longo.
    *   **Tradução**: Converter texto de um idioma para outro.
    *   **Geração de Texto**: Criar texto coerente e relevante.

## Capítulo 2: Text Classification

*   **Conjunto de Dados**: Introdução e **análise de um conjunto de dados** específico para a tarefa de classificação de texto, como a análise de sentimentos.
*   **Hugging Face Datasets**: Demonstração do uso da biblioteca **Hugging Face Datasets** para **carregar, inspecionar e processar conjuntos de dados** de forma eficiente.
*   **DataFrames**: Explicação da **conversão de objetos Dataset para DataFrames Pandas** para facilitar a análise e visualização dos dados.
*   **Distribuição de Classes**: Análise da **distribuição das classes** no conjunto de dados e a importância de identificar desequilíbrios.
*   **Comprimento dos Tweets**: Investigação do **comprimento das sequências de texto** (neste caso, tweets) e sua relevância para as limitações de contexto dos modelos Transformer.
*   **Tokenização**: Exploração do processo de **conversão de texto bruto em tokens**, as unidades atômicas de entrada para os modelos, abordando diferentes estratégias como **tokenização por caracteres, palavras e subpalavras**, incluindo o uso de `AutoTokenizer`.
*   **Tokenização Completa**: Demonstração da **tokenização de todo o conjunto de dados** usando a função `map` da biblioteca `Datasets`.
*   **Treinamento de Classificador**: Apresentação do processo geral de **treinamento de um classificador de texto** usando Transformers.
*   **Transformers como Extratores**: Uso de modelos Transformer **pré-treinados como extratores de características**, congelando seus pesos e treinando apenas uma camada de classificação sobre as representações extraídas.
*   **Ajuste Fino**: Explicação detalhada do **ajuste fino (fine-tuning)** de modelos Transformer pré-treinados em um conjunto de dados específico para a tarefa de classificação, atualizando todos os parâmetros do modelo para melhorar o desempenho.

## Capítulo 3: Transformer Anatomy

*   **The Transformer Architecture**: Exploração da arquitetura fundamental do Transformer, incluindo o **codificador** e o **decodificador**.
*   **The Encoder**: Análise detalhada do codificador, suas camadas de **autoatenção multi-cabeça**, camadas **feed-forward**, **conexões skip** e **normalização de camada**, além da importância das **incorporações posicionais**.
*   **The Decoder**: Visão geral do decodificador, destacando a **autoatenção mascarada** e a **atenção codificador-decodificador**.
*   **Meet the Transformers**: Apresentação das principais **famílias de modelos Transformer**: apenas codificador (ex: BERT), apenas decodificador (ex: GPT) e codificador-decodificador (ex: Transformer original, BART, T5) e suas aplicações.

## Capítulo 4: Multilingual Named Entity Recognition

*   **The Dataset**: Introdução a conjuntos de dados multilingues, como o **PAN-X**, para o reconhecimento de entidades nomeadas (NER) em diversos idiomas.
*   **Multilingual Transformers**: Exploração de modelos Transformer treinados em múltiplos idiomas, como o **XLM-RoBERTa**, e seu potencial para **transferência zero-shot** entre línguas.
*   **A Closer Look at Tokenization**: Análise detalhada da tokenização em contextos multilingues, incluindo o uso do **SentencePiece** em contraste com o WordPiece.
*   **Transformers for Named Entity Recognition**: Adaptação de modelos Transformer para a tarefa de NER, abordando a classificação de tokens e o tratamento de subpalavras.
*   **The Anatomy of the Transformers Model Class**: Explicação da estrutura modular da biblioteca Transformers, separando o "**corpo**" do modelo e as "**cabeças**" específicas para cada tarefa, permitindo a criação de modelos customizados.
*   **Tokenizing Texts for NER**: Processo de tokenização de textos para a tarefa de reconhecimento de entidades nomeadas, alinhando tokens com suas respectivas etiquetas.
*   **Performance Measures**: Métricas comuns para avaliar modelos de NER, como **precisão**, **recall** e **F1-score**, e a biblioteca `seqeval`.
*   **Fine-Tuning XLM-RoBERTa**: Demonstração do ajuste fino do modelo XLM-RoBERTa para a tarefa de NER multilingue.
*   **Error Analysis**: Técnicas para analisar os erros cometidos pelo modelo, identificando possíveis problemas no dataset ou no modelo.
*   **Cross-Lingual Transfer**: Avaliação da capacidade do modelo ajustado em um idioma de generalizar para outros idiomas sem treinamento adicional.
*   **When Does Zero-Shot Transfer Make Sense?**: Discussão sobre as condições em que a transferência zero-shot pode ser eficaz em comparação com o ajuste fino monolingue.
*   **Fine-Tuning on Multiple Languages at Once**: Exploração do treinamento de modelos em dados rotulados de múltiplos idiomas simultaneamente para melhorar o desempenho em todos eles.
*   **Interacting with Model Widgets**: Utilização dos widgets interativos no Hugging Face Hub para testar modelos diretamente no navegador.