# Emoji Disambiguation 🤔
This project used a Jypter Notebook to automate tagging the senses of each emoji. The results are datasets for disambiguating the most popular emojis. 

## The problem
- Emojis do not have explicit dictionary meanings like words
- They are ambiguous and subjective as their meanings are inferenced from text
- They do not have word equivalence and take on their own unique meanings
- They are extreme homonyms

e.g. Emojipedia interpretation of 'Upside-Down Face' 🙃 : Commonly used to convey irony, sarcasm, joking, or a sense of goofiness or silliness. 

<img width="760" alt="Screenshot 2023-10-05 at 11 37 19" src="https://github.com/elenabarry/Emoji-Disambiguation/assets/53048127/d23139ad-d40a-4d10-8e83-0b89124e049a">

## Emoji Embeddings

- Emoji embeddings are vector represenations of emoji meanings
- All current methods are not context dependent. Often key words describing the emoji are used to embed it
- This means the wrong meaning of the emoji is often assigned

<img width="382" alt="Screenshot 2023-10-05 at 11 34 34" src="https://github.com/elenabarry/Emoji-Disambiguation/assets/53048127/e5057a22-6b53-4ecc-bc4b-db90e25fdc99">

## The algorithm 

1. Given a Tweet with an emoji compute a sentence embedding of only the text - Using InferSent
2. Take the emoji of the corresponding Tweet. Embed all of its different senses.
3. Find the closest cosine similarity between the text of the Tweet and the emoji sense embedding. 

Image from 'One emoji, many meanings: A corpus for the prediction and disambiguation of emoji sense' who have implemented the first ever emoji lesk algorithm. 
<img width="353" alt="Screenshot 2023-10-05 at 11 39 06" src="https://github.com/elenabarry/Emoji-Disambiguation/assets/53048127/f965328b-64dc-4a4f-982b-ae6048841d1c">

## Dataset Methodology 

For each emoji, a distinctive collection of sense words were selected using WordNet using online dictionaries.

<img width="394" alt="Screenshot 2023-10-05 at 11 43 44" src="https://github.com/elenabarry/Emoji-Disambiguation/assets/53048127/d42d2b55-7c3e-4f25-b553-811122953208">

## Labelling Method

The open source software 'tortus' was used to label the dataset. Tweets were feed in and the senses were displayed as buttons below for the user to select the meaning of the emoji in context. 

<img width="741" alt="Screenshot 2023-10-05 at 11 46 57" src="https://github.com/elenabarry/Emoji-Disambiguation/assets/53048127/2347b34c-8e20-4ff6-a889-3f5603a33674">

## Datasets

The datasets ahve been double annotated and have a good Cohens Kappa score of 0.6, which is a measure of aggreement between the anatators taking into account random chance.

## Results of Datasets using Emoji-Lesk Algorithm

The most frequent sense (MFS) algorithm assigns the most frequent sense from the data.It is known that this approach is hard to outperform especially by unsupervised approaches like the Lesk algorithm. The new datasets not only improve the MFS algorithm by using concise senses, but can outperform the MFS algorithm where emojis are more ambiguous. 

<img width="209" alt="Screenshot 2023-10-05 at 11 48 24" src="https://github.com/elenabarry/Emoji-Disambiguation/assets/53048127/ddce5cfd-5701-41d9-8217-72139805e643">




