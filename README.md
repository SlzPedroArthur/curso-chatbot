# Meu Primeiro Chatbot: aprendendo PLN
O código fonte pode ser encontrado [aqui](https://colab.research.google.com/drive/10frZLPsIzafuW8cduvT6qlXIxAF0-t__).



1. PLN para o desenvolvimento de Chatbots;
    1. Tokenization
    2. Stemming
    3. Lemmatization
    4. Vectorization
    5. Word Embedding
    6. Reconhecimento de entidades nomeadas
    7. Classificação de texto;
2. Construindo um Chatbot Retrieval-Based
3. Intrgrando Redes Neuraris




## Tokenization

Tokenization é a tarefa de segmentar texto em palavras. Tokenization é importante para aplicações PLN, pois  a maioria das aplicações PNL utilizam palavras. Neste contexto, uma palavra pode ser definida utilizando o caractere de espaço “\s”. Por exemplo “A raposa pula em cima do coelho” pode ser dividida da seguinte forma:

[“A”, “raposa”, “pula”, “em”, “cima”, “do”, “coelho”]

Entretanto, utilizando apenas esta abordagem poderia acabar com exemplos como:

[“She’s”, “a”, “girl”, “wearing”, “a”, “blue”, “shirt”]

Para solucionar este problema, não podemos nos ater somente à separação pode por espaços. Um refinamento interativo pode ser aplicado antes da separação, fazendo com que tenhamos novos tokens usando expressões regulares. Assim,  “She’s a girl wearing a blue shirt” pode ser separado como:

[“She”, “is/’s”, “wearing”, “a”, “blue”, “shirt”]

A mesma abordagem pode ser usada para lidar com problemas de pontuação. “Is she wearing a blue shirt?” invés de ser separado como [“Is”, “she”, “wearing”, “a”, “blue”, “shirt”] deve ser separado como:

[“Is”, “she”, “wearing”, “a”, “blue”, “shirt”, “?”]

Expressões regulares devem ser usadas para separar todos os tipos de pontuação - pontos de interrogação, exclamação, finais, vírgulas, dois pontos, etc.

Usando este método, mais de 90% (PROCURAR REFERENCIA) dos problemas envolvendo Tolkenization pode ser resolvido.  

Para testarmos estas técnicas usaremos spaCy.  SpaCy implementa algoritmos no estado da arte na área de Processamento de Linguagem Natural. Podemos baixar o spaCy para a lingua portuguesa e inglesa em https://spacy.io/usage usando conda ou usando pip.


    $ pip install -U spacy
    $ python -m spacy download en_coreweb_sm
    $ python -m spacy download pt_core_news_sm















