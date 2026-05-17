DATASET: https://drive.google.com/drive/folders/16lHceA9Y0e3BMD6Ru3sOl7PP7yO2_s50?usp=drive_link
## Task 3: Text Vectorization
At the core, machine learning and neural networks are mathematical engines which use linear algebra, calculus, and probability. Due to this they cannot understand or "read" text strings hence requiring them to be converted into numerical vectors. 
## Task 5: Sequence Model and Conceptual Architecture:
Full model training for possible and successfully achieved 71% validation accuracy. LSTM architecture is designed to read text sequentially similar to how a human would process text which allows the model to know context rather than just bag of words.  
## Task 6: Attention and Transformer reflection:

**a. Why RNNs struggle with long term dependencies**

Recurrent Neural Networks process text sequentially, reading one word at a time and passing a memory forward. The problem here is Vanishing gradient problem, during training the network uses calculus to update it's weights. When such updates happen in a long sentence, as they travel backward, they get multiplied by small numbers over and over thus srhinking exponentially until they vanish. By the time RNN reaches the end of a paragraph, it has forgotten the words at the beginning because of the signal faded away. 

**b. How LSTMs help with the memory**

LSTMs fixed RNN's forgetting trait by introducing a dual-track memory system, alongside with the hidden state, LSTMs added a core Cell State like a conveyor belt running throughout the network, they also introduced "Gates" that act as intelligent guards, these Gates learn what is important enough to place on the conveyor belt like the main subject of a sentence. Because the cell state flows relatively uninterrupted, LSTMs can carry memory across much longer sequences.

**c. What Attention solves in sequence-to-sequence tasks?**

Even with LSTMs, early translation models had a major flaw, they had to compress an entire input sentence into a single fixed size vector before decoding it into French, Attention solved this by changing the input method, instead of compressing the whole sentence into one vector, it keeps all intermediate states. When the model translates a new word, it "looks back" at the entire orignial sentence and mathametically assigns a higher wieght to the specific words that are most relevant at that particular time. 

**d. Why Transformers are important in modern NLP and Gen AI**

Transformers completely changed how modern NLP and Gen AI worked, they removed the structure of RNN and LSTM structure and kept only Attention from it, leading to thr Self Attention mechanism which allowed models to process every single word in a document simultanouesly, rather than one-by-one from left to right. This helps with massive parellelization and Global Context making the model use GPUs to their limits and still maintain context/mathematical connection to every other word in the text. 