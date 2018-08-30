# helloGeneticAlgorithm
Simple genetic algorithm in Python to reach a fixed optimal DNA.

## Pseudocode
1. START
    * Generate the initial population
2. REPEAT UNTIL predefined max. generation is reached
    * Selection
    * Crossover
    * Mutation
    * Compute fitness

## Example Results

* Real sentence (Optimum DNA): "be the change that you wish to see in the world"
* **Length of real sentence: 47**
* Alphabet: lowercase letters and space 
* Number of of generations: 250
* Population: 2000
* Mutation percentage: % 0.01

| Generation | Average Score | Best 4 Scores  in generation | Worst 4 Scores in generation |
|:----------:|:-------------:|:----------------------------:|:----------------------------:|
|      0     |     1.7145    |          7, 6, 6, 6          |          0, 0, 0, 0          |
|     25     |     16.25     |        25, 24, 24, 24        |          8, 8, 8, 7          |
|     50     |     25.779    |        35, 34, 34, 34        |        17, 17, 17, 15        |
|     75     |     32.126    |        40, 40, 40, 40        |        24, 24, 24, 23        |
|     100    |     37.103    |        45, 44, 43, 43        |        29, 29, 29, 27        |
|     125    |     40.583    |        46, 46, 46, 46        |        34, 34, 31, 31        |
|     150    |    42.8635    |        47, 47, 47, 47        |        37, 37, 36, 36        |
|     175    |     44.399    |        47, 47, 47, 47        |        39, 39, 39, 39        |
|     200    |     45.117    |        47, 47, 47, 47        |        41, 41, 41, 40        |
|     225    |    45.7315    |        47, 47, 47, 47        |        40, 40, 40, 39        |
|     250    |    46.0415    |        47, 47, 47, 47        |        43, 43, 42, 42        |

### Best DNA's over generations

| Generation |              Best DNA in generation             |
|:----------:|:-----------------------------------------------:|
|      0     | dcnqwkenvtgllwqvz zicd zishbeoofumfknztjvsbuucc |
|     25     | qf tlwkchafgy bhateooc wish te heb pn tr dpgdwd |
|     50     | be tpe cvagge bhatkyom wish tooseb pn tkeow rld |
|     75     | ne tpe chafgy thax you wish to seb in the wodld |
|     100    | be the change that you wish te sei in the world |
|     125    | be the rhange that you wish to see in the world |
|     150    | be the change that you wish to see in the world |
|     175    | be the change that you wish to see in the world |
|     200    | be the change that you wish to see in the world |
|     225    | be the change that you wish to see in the world |
|     250    | be the change that you wish to see in the world |

### Worst DNA's over generations

| Generation |             Worst DNA in generation             |
|:----------:|:-----------------------------------------------:|
|      0     |  bcpiljmizhbbgxxubynymyoewkwiyejkhmrgkoeofyigvp |
|     25     | cfwx sgeojpgy tytznhcd opdcjtooipl pqyfwybrugwj |
|     50     |  jltpq e jpgqptaatkytuhpydcbtooski pnzt mfupalb |
|     75     | be qap c zfgy tbwu gdm zisk tooseidpnotrx wculd |
|     100    | zfipkg cvzfgy thau ysn wish te xjb in ty gworld |
|     125    | be qjs ehagge thztkyojgzish te xei pn cre world |
|     150    | beqqje c aggy thatkyou wish to seo pn thefwortd |
|     175    | be the chunge thau yim wish to qeb pn tte world |
|     200    | be the chuhge that kom wish to fee in the wonlf |
|     225    | be ehe change thateyou wish eo seb ix thefzortd |
|     250    | be the chafge thateyou pish to see qn the wortd |

## Notes

* Selection of an individual is directly proportional to square of its fitness score. For example:<br/>
   * Ind1.score = 1<br/>
   * Ind2.score = 2<br/>
   * Ind3.score = 3<br/>
So, the probability of selecting the **Ind3** is 3\*3 / (1\*1+2\*2+3\*3) = 9 / 14
* Crossover is done in 3 to 10 random points in a DNA.<br/>
   For example, let's say "1" represents the corresponding gene in a DNA of first individual and "2" represents gene of second individual.<br/>
   In the DNA below, there are 5 crossover points.<br/>
   111111**12**22222**21**1111111**12**2222222**21**1111**12**222222
