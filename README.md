
![Transformers](https://www.google.com/search?client=firefox-b-1-d&sca_esv=590541752&sxsrf=AM9HkKkheuE8ghed8mtt-1EWL3PR5X952w:1702472677148&q=transformer+ai&tbm=isch&source=lnms&sa=X&ved=2ahUKEwiS1KT5vIyDAxWmkiYFHeIQDMIQ0pQJegQIDBAB&biw=1128&bih=628&dpr=2#imgrc=_7u3z5YfFRHKeM)


## Transfomers as seen from space
Transformers refer to a class of deep learning models that are designed to handle sequential data efficiently, particularly in natural language processing (NLP) tasks. They have revolutionized the field of NLP due to their exceptional performance in various language-related tasks.

*Key Characteristics:*

**Attention Mechanism:** Transformers rely on a mechanism called "attention" to process sequential data. Attention allows the model to focus on specific parts of the input sequence when making predictions, capturing long-range dependencies more effectively than previous models.

**Self-Attention:** In a transformer, each input token attends to all other tokens in the sequence, enabling a better understanding of the context of each token within the entire sequence.

**Parallelization:** Transformers can process input sequences in parallel, making them computationally efficient compared to sequential models like recurrent neural networks (RNNs).

*Components of a Transformer Model:*

**Encoder-Decoder Architecture:** Transformers often consist of an encoder-decoder architecture. The encoder processes the input sequence, while the decoder generates the output sequence.

**Multi-Head Attention:** Transformers use multiple attention heads to capture different aspects of the input sequence simultaneously, enhancing the model's ability to learn complex patterns.

**Positional Encoding:** Since transformers do not inherently handle sequence order, positional encodings are added to the input embeddings to convey the positional information of tokens within the sequence.

*Applications:*

**Language Translation:** Transformers, such as the Transformer model introduced by Vaswani et al. (2017), have been highly successful in machine translation tasks.

**Language Understanding:** Transformers are used in various NLP tasks, including sentiment analysis, text generation, question answering, summarization, and named entity recognition.

**Pre-trained Models:** Large pre-trained transformer models like BERT, GPT (Generative Pre-trained Transformer), RoBERTa, and others have achieved state-of-the-art performance in various language understanding tasks. These models are often fine-tuned for specific downstream tasks.

Transformers have significantly advanced the capabilities of natural language processing models, enabling more accurate and context-aware understanding and generation of human language. Their versatility and effectiveness have made them a cornerstone in the field of NLP and beyond.

## Mathematics under the hood
#### Word Embeddings: Example - I love data science

Now, let's calculate the word embeddings in two dimension for simplicity. In reality, it is often 512 dimensions but could be any. With respect to I, the 1 or 0 are asigned as:

I love data science
1   0    0     0  

Since, we're dealing with only two dimensions above numbers are multipled with weights to generate new pair of word emeddings. For example, 1 is multiplied with 1.87 and 0.09 and thus the word embedding for **I** is now **[1.87, 0.09]**. Word embeddings for **love**, **data**, and **science** are calcualted in similar way.

As of now we have:
input_sequence = ['I', 'love', 'data', 'science', <eos>]
And word embeddings in two dimension for each of these.

Now, an alternating sine and cosine magnitude for each token and for each embedding is calculated. This value is added to each embedding to get a position encoded word embedding.
Then transformer applies linear transformation to the position encoded embeddings to obtain query (Q), keys(K), and values(V) by multiplying with these weight matrices.

Q = E.Wq 
K = E.Wk
V = E.Wv

Where, E is position encoded embeddings, and W is weight matrices for querey, keys, and values.




