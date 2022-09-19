# Wikipedia-Graph analysis
##### The analysis done previously can be found in the "Naive" directory. The name only suggests that the coming approaches will be more sophisticated.<br>
##### Dataset that can be used : 
1. [Wikispeedia navigation paths](https://snap.stanford.edu/data/wikispeedia.html)
2. [Wikipedia networks](https://snap.stanford.edu/data/wikipedia-article-networks.html)

##### Useful link to save notebook state: [Save notebook state](https://stackoverflow.com/questions/34342155/how-to-pickle-or-store-jupyter-ipython-notebook-session-for-later)
#### Below is a tentative plan to do this analysis in a systematic manner:
```mermaid
graph TD;
A[Collect all links from initially labelled pages]--->B[Construct Graph using wikipedia pages];
A--->C[Extract NLP feature vector for each page];
B--->D[Enrich the NLP feature vector along with the graph structure information using GNNs];
C--->D;
D--->F[Provide similar pages to given wikipedia page];
E[Given a new wikipedia page]--->F;

```
