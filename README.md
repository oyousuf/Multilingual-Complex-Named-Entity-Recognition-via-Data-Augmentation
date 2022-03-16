# Multilingual-Complex-Named-Entity-Recognition-via-Data-Augmentation

As part of The 16th International Workshop on Semantic Evaluation (SemEval 2022) [Task 11: MultiCoNER
Multilingual Complex Named Entity Recognition](https://multiconer.github.io/), this repository contains a template inspired by [Simple Data Augmentation for Named Entity Recognition](https://aclanthology.org/2020.coling-main.343.pdf).

The [template notebook](https://github.com/oyousuf/Multilingual-Complex-Named-Entity-Recognition-via-Data-Augmentation/blob/main/template.ipynb) comments through the code for each of the 4 basic data augmentation methods and also 2 more optional methods.

Formatting of the named entity recognition (NER) files is [.conll](https://universaldependencies.org/format.html). Entities considered for this task were PROD (Person), GRP (Group), CORP (Corporation), CW (Creative Work), PER (Person), LOC (Location), O (other, none, N/A). Other entities in an NER.conll file could be applied, but you would have to alter the template code as you see fit. The beginning of each named entity begins with an identifier (# id ...).

Examples of the original format can be seen in the [format_and_augmentation_examples](https://github.com/oyousuf/Multilingual-Complex-Named-Entity-Recognition-via-Data-Augmentation/tree/main/format_and_augmentation_examples) folder. I've included 2 of the 11 SemEvall 2022 languages as reference. For example, 'en_train.conll' is your original ner file and other files in the same folder are the outputs of the various data augmentations. Getting familiar with the data augmentation methods is recommended before applying ([see paper](https://aclanthology.org/2020.coling-main.343.pdf)).

The only data augmentaiton method that requires something other than an ner file is the synonym replacement option. The code makes use of a pretrained word vector for a specific language. I used [fastText word vector trained on Wikipedia](https://fasttext.cc/docs/en/pretrained-vectors.html). You can find your language, download the 'bin+text' option and that will be your path for the synonym replacement part of the code.
 * Note: pretrained word vectors are not that great for low-resource languages, this can be moderately observed in the presentation of my findings [here](https://github.com/oyousuf/Multilingual-Complex-Named-Entity-Recognition-via-Data-Augmentation/blob/main/Presentation.pdf), but it's  always worth experimenting with for your language.
