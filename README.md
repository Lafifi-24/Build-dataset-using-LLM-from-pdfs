# objective
we have at hand two pdf files that describes risk factors related to a financial trade (two documents
each for its own trade), the use of our chatbot want to get answers based on the knowledge of the
documents.

example

user: show me an outline of the risk factors

chatbot: the risk factors outlined in the first document are:
- 1. …
- 2. …
    - a. …
    - b. …
- 3. … 

And the risk factors outlined in the second document are:
- 1. …
- 2. …
- 3. …
    - a.
    - b.
    - c.
    - d.
- 4. …
    - a. …
    - b. …
    - i. …
- 5. …

### Plan
I present two notebooks:
#### Data preparation
- Read PDFs and analyzed.
- Built datasets and prepared them to be used in the RAG system.
    - To prepare the datasets, I split the two PDFs into similar paragraphs by detecting their titles.
    - Then, I used GPT-4 to create questions and their answers for each paragraph.
#### Build chat
- I used "all-MiniLM-L6-v2" as the embedding model.
- and Chroma as the default database; it uses L2 to calculate similarity.
- I used "mistralai/Mistral-7B-Instruct-v0.2" for generating answers.
- Then, I used GPT-4 to score the Mistral answers.
- At the bottom of the notebook, I explain other approaches we can apply to get more accurate answers.

#### usage 
- install packages in requirements file. 
