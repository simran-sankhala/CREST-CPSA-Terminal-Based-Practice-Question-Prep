# CREST-CPSA-Terminal-Based-Practice-Question-Prep
a mini docker container running php which supports simulation of questions from a csv file in cli with real time correct/wrong answer prompt

### Folder Structure
```bash
$ tree
.
├── Dockerfile
├── exam
├── Flashcards
│   ├── Exam
│   │   ├── ScoreKeep.php
│   │   └── Timer.php
│   └── Exam.php
├── autoload.php
├── questions.json
└── README.md
```
2 directories, 8 files

## Build
```bash
$ docker build -t crest-cpsa-exam .
```

## Run & Deploy
```
$ docker run --rm -ti crest-cpsa-exam
```

## Modify Exam question count

Individual tests can be generated like this:

```bash
# Unset for individual set of 120 questions
CMD ["/usr/local/bin/php","-f","exam","crest-cpsa-exam.json","120"]
```
