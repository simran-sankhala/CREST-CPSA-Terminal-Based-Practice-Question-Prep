<div style="display:flex; justify-content:center; align-items:center;"><img src="https://www.crest-approved.org/wp-content/uploads/2022/04/Crest-logo-Refresh_2022_CMYK_2_AW_col-no-reg-TM-scaled.jpg" style="width:500px;"></div>


  
  
# CREST-CPSA-Terminal-Based-Practice-Question-Prep
  
  
a mini php application running docker container which supports simulation of questions from a json file in cli with real time correct/wrong answer prompt

  

### Folder Structure
![](tree.png)

## Build
```bash
$ docker build -t crest-cpsa-exam .
```
![](build.png)

## Run & Deploy
```
$ docker run --rm -ti crest-cpsa-exam
```

## yay it works !! 🥳

![](poc.png)

## Modify Exam question count

Individual tests can be generated like this:

```bash
# Unset for individual set of 120 questions
CMD ["/usr/local/bin/php","-f","exam","crest-cpsa-exam.json","120"]
```
