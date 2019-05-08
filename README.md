# drilbot: GPT-2 finetuned on dril twetes

I trained GPT-2 (medium) with [minimaxr's](https://github.com/minimaxir) notebook on ~2600 dril tweets. Some results, chosen at random:

> * i have spent many a sleepless night researching the various anti-mother, anti-father sentiments that are commonly espoused by the "Moms"
> * please help me
> * because they say in the occult, every once in a while, that shit goes wrong...
> * people keep asking how i became blind in one eye. the truth is that i lost my left eye during in the greatest shit of all time
```

Overall, to quote the bot, >i think its fucking awesome

## How it works

**Data Gathering** I gathered the data using [twint](https://github.com/twintproject/twint).

**Training** Finetuned the data using [minimaxr's extremely awesome notebook](https://colab.research.google.com/drive/1VLG8e7YSEwypxU-noRNhsv5dW4NfTGce). I used the 345M parameter model. Couple of tips that helped me train:
- The model overfit. I trained at a lower rate (1e-5) and stopped the model after 1000 steps to prevent this. It was *just* after the model seemed to be taking on the dril style. A good hallmark was the appearance of my custom tweet separation token (SEP).
- The initial tweets I generated were quite repetitive, so I increased the temperature to 1
- Otherwise, didn't try to tune too many parameters

## Results

I threw 10k fake tweets in `generated_tweets.txt`. Here are a bunch of samples (umm, NSFW):

> * no thats not it, i love thinking of new and creative punishments for people who piss me off. such as a swollen ass after using too many mouthwash bottles, or being spat on in a dangerous spot
> * looking forward to seeing how polite texas congresspeople are when they finally decide to enact true sentencing reform .
> * wait a sec, the only thing "Anus" can give birth to is.....shit
> * i invented a way for my 5'2 self to scrape together the cash to completely hose my body in a wide variety of pesticides, all while maintaining the stunning physique and bony remains you see displayed on tv
> * ochestver i will now be addressing the people of sioux hall again. for the rest of my life people think im some sort of dip shit, for borrowing people's nicknames and making fun of them for having high functioning autism
> * now the threads are flooded with people telling me to fup , to fart, to ruin the fun of science. FUCK
> * ive always wanted to put a paint stripper through my pud but ive been told by Pip thats his fault for ban him from the shower .... ENABLED
> * APOLOGIZING FOR LATE VIDEO CONTENT. MY STUPID ASSES SHOT MY SEXUALLY.:/
> * DEAD AT FILM'S INSPIRATION of "SCOTT VAULT JACKSON" , OF
> * producers attempt to agitate Mary Poppins fans at the movie theater lobby with sounds of cheap tickets as hard liquor is poured on the group
> * aveted trailer for "373 boys"- a 71% respeckned 2011 minigun (upgraded to a $120k cannon) that promptly fails all safety tests
> * my worker quesiton: which shows higher average will lead to accepted story direction. will lead to accepted story direction.
> * frightened ot miss out on the chance to win a rare beAUTiful Parrot Futuronair
> * elmer normalized
> * penning another "Hasta Pt To Wendy" letter on my 80 year old mother
> * wendys are good at making you believe that your friends and family think youre funny and smart . until you ask
> * ive deleted myself from facebook after reading a story about a guy whose penis got stuck to the wall and had to be removed
> * NO w Alexander! NO more "bhavin oy vegas" blow up after blow up.
> * my fav SVN algorithms may or may not be bad, but they certainly cant save my life
> * lunch is always welcome at my house. my go-to drinks being……. (sips beer) a little lagery, a lot of gin, and a few shots of rum
> * please do not take my word for it. get a part-time Data Scientist to do a google image search of "zach de la Riong sex tape" , and post it in this angry fave tom boy's
> * deviantART IS CRIMINAL, and theyre the SAME THING. Bitch
> * ill never dance on another dog face (from a distance) 
