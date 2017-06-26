### Perform sentiment analysis using an RNN

### Dataset information:
- Dataset obtained from Udacity

### Models
- [explained model](https://github.com/JackBurdick/nlp_sentiment_rnn/blob/master/sentiment_rnn_explained.ipynb)
    - contains many notes
- [expanded model](https://github.com/JackBurdick/nlp_sentiment_rnn/blob/master/sentiment_rnn_expanded.ipynb)
    - more advanced preprocessing techniques used

The performance between the two models is minimal.  Interestingly, the "simple"[explained model](https://github.com/JackBurdick/nlp_sentiment_rnn/blob/master/sentiment_rnn_explained.ipynb) outperforms the model that includes more advanced techniques [expanded model](https://github.com/JackBurdick/nlp_sentiment_rnn/blob/master/sentiment_rnn_expanded.ipynb) by ~2% ACC.

### Performance
The performance here is, in my opinion, trivial.  There are many issues;
 - How _good_ is this dataset, we're assuming it's *perfect*
    - Are there any neutral reviews. How was pos/negative assigned
 - Analysis could be performed at the sentence level, not entire review
    - Do reviews contain positive any negative sentences in the same review? They likely do.
        - The classification could become a muli-class; various degrees of pos/neg and neutral.
 - How subjective is the label?


## TODO:
 - include figures of models in readme
 - shuffle index
 - save "best" model, not last model
    - Use `early stopping`, if unable to find method to save the best model (either by val_acc or loss)
 - create plots of the losses
 - investigate the section `Review the current state/information about our data`
    - the results do not affect the outcome, but the logic may be flawed

