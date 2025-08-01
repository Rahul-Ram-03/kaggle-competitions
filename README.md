### [int-ext-pred](https://github.com/Rahul-Ram-03/kaggle-competitions/blob/main/int-ext-pred.ipynb)
Predict introivert/extrovert from data. Link to competition [here](https://www.kaggle.com/competitions/playground-series-s5e7).
<br>
### [impostor-txt-pred](https://github.com/Rahul-Ram-03/kaggle-competitions/blob/main/impostor-txt-pred.ipynb)
Link to competition [here](https://www.kaggle.com/competitions/fake-or-real-the-impostor-hunt/overview)<br>
<b>Approach 1</b>: A transformer encoder with 3 linear layers to determine the boolean value/prediction.<br>
<b>Approach 2</b>: Concat the input tokens, separate them using a [SEP] token and pass the concatenated input to the model. The idea behind this approach is to provide the <br>transformer with the input token simultaneously, so that it can somehow learn to contrast the two texts. Scored the worst out of all three approaches.<br>
<b>Approach 3</b>: Dual encoder approach: pass in the inputs separately, concat the embeddings from the encoder and then pass that into the linear layers. Essentially, the <br>responsibility of comparing the two texts fall onto the linear layers. Scored the best out of all three approaches.