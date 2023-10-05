# Emoji Disambiguation
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



<img width="902" alt="Screenshot 2023-10-05 at 11 21 14" src="https://github.com/elenabarry/Emoji-Disambiguation/assets/53048127/3ef58414-dc09-46de-88be-7a6423670147">


![Screenshot 2023-10-05 at 11 18 49](https://github.com/elenabarry/Emoji-Disambiguation/assets/53048127/a53230a9-029e-481e-aa96-b90f4eca6f47)
