# LongShortTermMemor-Network-LSTM

## implementing Encoder-Decoder scheme
For sequence-to-sequence prediction issues, the encoder-decoder strategy for recurrent neural networks is an architecture.

- Encoder: The encoder is in charge of walking through the input time steps and encoding the complete sequence into a context vector, which is a fixed length vector.

- Decoder: The decoder is in charge of reading from the context vector while stepping through the output time steps.

- Sequential:A sequential approach is suited for a simple stack of layers with one input tensor and one output tensor for each layer.

- return_sequences: By default its set to False. Whether to return the last output in the output sequence, or the full sequence.

Input Shape:the input shape is generally the shape of the input data provided to the Keras model while training. As we now the input data queries and answers are fixed as 5 × 13 and4 × 13, respectively.

## LSTM
The Long Short Term Memory Network (LSTMN) is an enhanced RNN (sequential network) that permits information to be stored indefinitely. It can deal with the vanishing gradient problem that RNN has. For persistent memory, a recurrent neural network, also known as RNN, is used.

- LSTM consists of three parts:

 - irrevelant information(Forget Gate)
 - add/update new information(Input Gate)
 - passing updated information(Output gate)


 ![image](https://user-images.githubusercontent.com/104048277/216736560-44bb9034-9b49-4b6d-8f9c-6420f7ac0bb6.png)

Let us suppose

H(t-1) represents hidden state of previous time stamp
Ht current time stamp
C(t-1) and C(t) for previous and current timestamp respectively

![image](https://user-images.githubusercontent.com/104048277/216736643-e4bfa6a9-f65b-41ea-810c-f755f299bdda.png)

- Output= Softmax(Ht)

 - Xt: the current timestamp's input.
 - Uf: the input's associated weight
 - Ht-1: The previous timestamp's hidden state
 - WF: The weight matrix associated with the concealed state is Wf.
 - Ui: weight matrix of input
 - Wi: Weight matrix of input associated with hidden state
