# ghigliottin-AI.github.io

### Task Description
Language games draw their challenge and excitement from the richness and ambiguity of natural language, and therefore have attracted the attention of researchers in the fields of Artificial Intelligence and Natural Language Processing.
For instance, IBM WatsonTM is a system which successfully challenged human champions of Jeopardy!TM, a game in which contestants are presented with clues in the form of answers, and must phrase their responses in the form of a question [[1]](#1). Other researchers exploited question answering techniques to build an artificial player for _“Who Wants to be a Millionaire?”_ [[2]](#2). Another popular language game is solving crossword puzzles. The first experience reported in the literature is Proverb [[3]](#3), that exploits large libraries of clues and solutions to past crossword puzzles. WebCrow is the first solver for Italian crosswords [[4]](#4).

Following the first edition of the NLP4FUN task [[5]](#5), proposed at EVALITA 2018, we propose a new edition of the task which aim is to design a solver for “The Guillotine” (La Ghigliottina, in Italian) game. It is inspired by the final game of an Italian TV show called “L’eredità”. The game, broadcast by Italian national TV, involves a single player, who is given a set of five words - the clues - each linked in some way to a specific word that represents the unique solution of the game. Words are unrelated to each other, but each of them has a hidden association with the solution. Once the clues are given, the player has one minute to find the solution. For example, given the five clues: pie, bad, Adam, core, eye the solution is apple, because: apple-pie is a kind of pie; bad apple is a way to refer to a trouble maker; Adam’s apple is the prominent part of men's throat; apple core is the center of the apple; apple of someone's eye is way to refer to someone’s beloved person.  “La Ghigliottina” is a challenging language game which demands knowledge covering a broad range of topics. Artificial players for that game can take advantage of the availability of open repositories on the web, such as Wikipedia, that provide the system with the cultural and linguistic background needed to understand clues [[6]](#6). 
Participants should build an artificial player able to solve “La Ghigliottina”.

### Data Format
We will provide a set of both training and testing games in JSON format:

```json
{
  "games":[
  {
        "id":1000,
        "clues":["uomo","cane","musica","casa","pietra"],
        "solution":"chiesa"
  },
  {
        "id":1001,
        "clues":["doppio","carta","soldi","pasta","regalo"],
        "solution":"pacco"
  }
  ]
}
```

The JSON file consists of an array of *games* which contains several JSON objects for each game. Each *game* has an identifier (*id*), an array of five *clues* and one *solution*.

The challenge is organized with the support of Ghigliottiniamo, a mobile app available both for [Android](https://play.google.com/store/apps/details?id=io.quiztime.game&hl=en) and [iOS](https://apps.apple.com/it/app/ghigliottiniamo/id1447355292), to let people challenge each other live on the ghigliottina games aired on TV. 
In a recent effort, Ghigliottiniamo has implemented an API to allow artificial solvers to take part in the competition. We will adopt this API to evaluate the systems participating in the EVALITA challenge. 
All participants will obtain instructions on how to connect their system to the Ghigliottiniamo server. We will provide a JSON file containing 300 games along with their solution to be used as training data. The participants can integrate any knowledge resources in their systems except further games. In the evaluation window, 100 games (without solution) will be sent via API from the Ghigliottiniamo server to the systems enrolled in the challenge, which in turn will have to reply with the solution.
We will exploit the evaluation approach implemented in Ghigliottiniamo which takes into account the accuracy of the system in predicting the correct solution. Moreover, we will try to compare the performance of artificial players with the ones of the users (humans) of the mobile app. This is the first time that we can compare artificial players against humans.

### References
[<a name="1">1</a>] D. Ferrucci, E. Brown, J. Chu-Carroll, J. Fan, D. Gondek, A. A. Kalyanpur, A. Lally, J. W. Murdock, E. Nyberg, J. Prager, N. Schlaefer, and C.Welty, “Building Watson: An overview of the DeepQA project,” AI Magazine, vol. 31, no. 3, pp. 59–79, 2010.

[<a name="2">2</a>] P. Molino, P. Lops, G. Semeraro, M. de Gemmis, and P. Basile. Playing with knowledge: A virtual player for who wants to be a millionaire? that leverages question answering techniques. Artificial Intelligence, vol. 222, pp. 157-181, 2015.

[<a name="3">3</a>] M. L. Littman, G. A. Keim, and N. Shazeer, “A probabilistic approach to solving crossword puzzles,” Artificial Intelligence, vol. 134, pp. 23–55, 2002.

[<a name="4">4</a>] M. Ernandes, G. Angelini, and M. Gori, “A web-based agent challenges human experts on crosswords,” AI Magazine, vol. 29, no. 1, pp. 77–90, 2008.

[<a name="5">5</a>] P. Basile, M. de Gemmis, P. Lops, and G. Semeraro, Solving a complex language game by using knowledge-based word associations discovery. IEEE Transactions on Computational Intelligence and AI in Games, vol. 8, no. 1, pp. 13-26, 2016.

[<a name="6">6</a>] P. Basile, M. de Gemmis, P. Lops, and G. Semeraro, “Solving a complex language game by using knowledge-based word associations discovery”, IEEE Transactions on Computational Intelligence and AI in Games, vol. 8, no. 1, pp. 13-26, 2016.


---

### Organizers
* Pierpaolo Basile, Dipartimento di Informatica, Università degli Studi di Bari Aldo Moro, pierpaolo.basile@uniba.it 
* Lucia Siciliani, Dipartimento di Informatica, Università degli Studi di Bari Aldo Moro, lucia.siciliani@uniba.it 
* Federico Sangati, Università di Napoli "L'Orientale" federico.sangati@gmail.com 
* Johanna Monti, Università di Napoli "L'Orientale", jmonti@unior.it 
* Antonio Pascucci, Università di Napoli "L'Orientale", apascucci@unior.it 
* Marco Lovetere, Ghigliottiniamo, marlove@gmail.com 

### Contacts
If you have any questions, please contact us: <ghigliottinai.evalita@gmail.com>
