---
layout: essay
type: essay
title: "The Importance of Smart Questions"
# All dates must be YYYY-MM-DD format!
date: 2023-09-21
published: true
labels:
  - Programming
  - Coding Standards
  - ESLint
---
<p align="center">
<img class="img-fluid" src="../img/eslint/eslint.png">
</p>


## 
&nbsp;&nbsp;&nbsp;&nbsp; Communication is one of the essential skills a software engineer needs to develop. Furthermore, asking 'smart' questions can be considered one of the most important communication skills from a professional perspective. But what is considered a smart question anyway? 
<br> 
&nbsp;&nbsp;&nbsp;&nbsp; In general, a smart question can be seen as one that is well-thought-out, informed, and designed to elicit meaningful information. In the context of software engineering where the majority of questions are asked on online forums like StackOverflow, the previously mentioned characteristics still remain true but there are also new aspects we must consider. 
<br>
&nbsp;&nbsp;&nbsp;&nbsp; First off, having a descriptive and meaningful title can increase your chances of your post getting clicked on and viewed in the first place. In the meat of the post, the problem should be descriptive and should also be followed with the goal you had in mind. For programming/code questions, this can be done by posting your broken code and describing in detail what it is supposed to do. Asking questions in this way not only increases your chances of getting them answered but can also help other people who run into the same issue down the line. 

## A Smart Question
&nbsp;&nbsp;&nbsp;&nbsp; Throughout the millions of posts on StackOverflow, here is one example of a user who asked a smart question in the post titled, ["JavaScript property access: dot notation vs. brackets?"](https://stackoverflow.com/questions/4968406/javascript-property-access-dot-notation-vs-brackets)
```
Q: Other than the obvious fact that the first form could use a variable and not just a string literal,is there any reason
to use one over the other, and if so under which cases?

In code:

// Given:
var foo = {'bar': 'baz'};

// Then
var x = foo['bar'];

// vs. 
var x = foo.bar;

Context: I've written a code generator that produces these expressions and I'm wondering which is preferable.
```
&nbsp;&nbsp;&nbsp;&nbsp; In this example, the user's title is quite straightforward and is able to convey the question without needing any extra context as it is asking for the difference between using two different property access methods as well as the language it is referring to (JavaScript). In the body of the post, the user provides us with a very basic code example to help us readers understand with more detail what the question is trying to convey. Additionally, this post has quite a lot of upvotes and helpful responses meaning many others have had this question as well, myself included. 

## A Not-So-Smart Question
&nbsp;&nbsp;&nbsp;&nbsp; It would be amazing if all the questions posted online were smart. Unfortunately, that is not the case as we have this post titled, ["where are the syntax errors am getting?"](https://stackoverflow.com/questions/30449692/where-are-the-syntax-errors-am-getting)
```
Q: I am making a program to simulate a game show, randomly. The program picks 1 of three doors for the prize to be hidden
behind randomly. The computer picks a door to see if it won or not. This is looped over 10000 times to see how many times
I win if I change my pick versus not changing it.

I am getting a bunch of syntax

#include  <path-spec>
#include <stdio.h>
#include <time.h>

void count(Status result, Door* pLast_pick, Door* pPick, int* pWin_unchanged, int* pWin_changed);

void randomize_door(Door* pJackpot);

void pick_door(Door* pPick);

Status check(Door* pPick, Door* pJackpot);

enum status {WIN=1,LOSE};

enum door { FIRST=1, SECOND, THIRD };

typedef enum door Door;
typedef enum status Status;

int main(int argc,  char* argv[]){
    int i = 0;
    srand(time);
    Status result;
    Status* pResult = &result ;
    Door jackpot, pick, last_pick=NULL;
    Door* pJackpot = &jackpot, * pPick=&pick, *pLast_pick;
    int win_unchanged = 0, win_changed=0;
    int* pWin_unchanged = &win_unchanged, *pWin_changed=&win_changed;

    while (i < 10000){
        last_pick = NULL;
        randomize_door(pJackpot);
        pick_door(pPick);
        result = check(pPick, pJackpot);
        count(result, pLast_pick, pPick, pWin_unchanged, pWin_changed);

        i++;
    }

    printf("Wins when changed choice: %d  , wins when choice is unchanged: %d", win_changed, win_unchanged);
    return 0;
}

void randomize_door(Door* pJackpot){

    *pJackpot = rand() % 3 + 1;
}

void pick_door(Door* pPick){

    *pPick = rand() % 3 + 1;
}

Status check(Door* pPick, Door* pJackpot){
    if (*pPick == *pJackpot){
        return WIN;
    }
    else{
        return LOSE;
    }
}

void count(Status result, Door* pLast_pick, Door* pPick, int* pWin_unchanged, int* pWin_changed) {
    if (*pLast_pick == *pPick){
        if (result == WIN){
            *pWin_unchanged++;
        }
    }
    else{
        if (result == WIN){
            *pWin_changed++;
        }
    }

    *pLast_pick = *pPick;
}

```
&nbsp;&nbsp;&nbsp;&nbsp; In this example, the title is not descriptive at all and contains a typo as a bonus. As a result, this question is not very searchable and people who may have the same issues have a lower chance of finding it. Getting into the body of the post, this user posts the error messages they encounter (shown in the original post) which explicitly tell them where the syntax errors are happening and what is causing them, therefore answering their own question. An important thing to note is there are many online resources on C syntax that the user could have referenced to solve this issue. However, the existence of this post shows that the user did not make an effort to search for the solution and jumped straight into StackOverflow.
