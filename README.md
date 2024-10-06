# BERT - Modelo de Linguagem

Esse projeto foi feito para a disciplina de mestrado da Unicamp IA024 - Redes Neurais Profundas para Processamento de Linguagem Natural.

Neste projeto, são utilizados Embeddings gerados por um BERT pré-treinado e uma MLP para prever a próxima palavra (token)

A base de dados utilizada foram textos retirados de livros do Machado de Assis (https://github.com/ethelbeluzzi/projetomachado)

As instruções foram:

Criar um modelo de linguagem e medir a perplexidade utilizando o dataset do Machado de Assis, utilizando Embeddings gerados por um BERT pré-treinado e uma MLP.

- Deve-se implementar o próprio laço de treinamento. Não usar frameworks de treinamento automático.
- Utilizar o BertModel.from_pretrained e BertTokenizer.from_pretrained do Hugging Face para carregar o BERT pré-treinado.
- Não utilize outras classes da HuggingFace/Transformers alem da BertModel e BertTokenizer.
- Trabalhe no espaço dos tokens/inteiros. Uma forma de fazer isso é tokenizar o dataset inteiro como pré-processamento.
- Experimente com aumentar o contexto e congelar ou não os parâmetros do BERT. Cuidado que o contexto é o maior fator para o peso computacional aqui.
- Sugerimos utilizar um BERT treinado em português como o BerTimbau: "neuralmind/bert-base-portuguese-cased".
- Inicialmente utilizar o hidden_state do token CLS. Podem experimentar com outras formas de usar o last_hidden_state.
- MLP deve utilizar o vocab_size do BERT na saída. Isso gera um grande desafio de manter o tamanho da MLP razoável.
