# drilbot
GPT-2 finetuned on dril twetes

I trained GPT-2 (medium) with [minimaxr's](https://github.com/minimaxir) notebook on ~2600 dril tweets. Some results:

```
i have spent many a sleepless night researching the various anti-mother, anti-father sentiments that are commonly espoused by the "Moms"

please help me

because they say in the occult, every once in a while, that shit goes wrong...

people keep asking how i became blind in one eye. the truth is that i lost my left eye during in the greatest shit of all time

the worst thing you can possibly do is offer to donate a kidney to htee.(18yrs old) i am appalled as by far the most heartless Person that you may EVER meet
```

Overall, to quote the bot, `i think its fucking awesome`

## How it works

**Data Gathering** I gathered the data using [twint](https://github.com/twintproject/twint).

**Training** Finetuned the data using [minimaxr's extremely awesome notebook](https://colab.research.google.com/drive/1VLG8e7YSEwypxU-noRNhsv5dW4NfTGce). I used the 345M parameter model. Couple of tips that helped me train:
- The model overfit. I trained at a lower rate (1e-5) and stopped the model after 1000 steps to prevent this. It was *just* after the model seemed to be taking on the dril style. A good hallmark was the appearance of my custom tweet separation token (SEP).

## Results

I threw 10k fake tweets in 