# UPDATE: For the pull request homework: Don't worry if the PR can merge, go ahead and make the PR. That is sufficient for completion of the assignment.


# Week 11: Reinforcement lab
Welcome to week 11 where we will do a reinforcement lab.

Let's take a look at the standard diagram (credit ref. [1])

![](https://github.com/alonzi/DS-3001/blob/a41a636f4cba7ad7869342056b8f3e90dc4507d8/week-11-reinforcement-lab/reinforcement.jpeg)

Ok, that was a dad joke, I couldn't help myself. That diagram is about Reinforcement Learning. Let's get to what we really mean, reinforcing the concepts from the past few weeks. The way we are going to do that is review, question, explore. (also known as KWL ref. [2]).

## A little about Pete
1. PhD in particle physics
2. Lead of Research Computing for the School of Data Science
3. LPA2A@virginia.edu

## Goals for Today
* Reinforce your understanding of previous topics 
* Everyone makes a PR to this repo (details at end, graded on completion)

# Part 1: Review
The syllabus shows the past few weeks have focused on
* Supervised KNN or Kmeans
* Evaluation metrics

## Exercise 1: What do you know?
For this exercise we will work in your teams.

1. There are 10 minutes on the clock
2. Discuss what you know and note those things
3. If you bump into something you know now write that down too in a different spot.

All together: Tell the room what you all wrote down

## Exercise 2: What do you want to know?
You get the drill, 10 mintues are on the clock.

1. Discuss with your team what you want to know. Where are you shaky? Where would you like more time to practice?
2. N.B.: This is tricky, you need to put yourself out there, trust your partners, be vulnerable.

All together: Tell the room what you want to know, what questions do you want to answer, where do you want to reinforce?

# Part 2: Explore
In part two we are going to rip into some data and explore. The overall goal is to reinforce what you started to learn in the past few weeks. Keep your questions in mind as we go, let them guide you. If you want to take a scenic route because it will help to reinforce, do it. Remember the goal is reinforcement, not completion of some assignment (you can always finish it for homework).


## Today's Dataset
* We will be using a mystery dataset today: [mystery data](https://github.com/UVADS/DS-3001/blob/main/week-11-reinforcement-lab/data-frame.csv)
* Courtesy of 17 lands, ref [3]
* N.B.: if you look at the url you will note it comes from s3.amazonaws.com

## Exercise 3: Let's Get the Ball Rolling
### Demo 
1. Download the data (hint: click the link above, it should open a download)
2. Unzip the data (hint: `tar -xzf game-data.MID.PremierDraft.tar.gz`)
3. Make an abbreviated data file (hint: `head -n 1000 game_data_public.MID.PremierDraft.csv > data-summary.csv`)
4. Load the data into a dataframe (hint: see scratch.R)
5. Select relevant columns: main_colors,opp_colors,on_play,num_turns,won (hint: see scratch.R) 
7. **Hardest Step:** compute two correlation metrics using the 271 features starting with 'deck_' (hint: see scratch.R lines 7-21, and ref [4] for extra credit)
### Start here
8. Download data from [repo](https://github.com/UVADS/DS-3001/blob/main/week-11-reinforcement-lab/data-frame.csv)
9. Make scatter plot of the two correlation metrics (hint: see scratch.R)
10. Stare at this plot for a long time, note what thoughts arise


## Exercise 4: Challenge
![](https://github.com/alonzi/DS-3001/blob/1c4895d217dfc6decdfce5f4e7647b12f7610e45/week-11-reinforcement-lab/podracing.gif)

Now explore, get creative, answer your questions, reinforce what you have learned. From looking at the scatter plot you will have ideas emerge, follow where they lead. This is where we get into the goal of today, answering our questions and reinforcing. Here are some ideas to help get you moving:
* apply knn or kmeans
* why cluster? what are you learning from clustering
* compare your clusters with other features in the dataset
* use more ggplot features like `color` and `size` in `aes(...)`


# Part 3: Reflect
In teams: Reflect on what you have learned and reinforced

All together: Tell the room what you have learned

# Part 4: Clean up
The final part of this assignment is to make a pull request
1. fork this repo: https://github.com/alonzi/DS-3001
2. create a file called [uvaNetID].R in the folder assignment-submissions (eg for me: assignment-submissions/LPA2A.R)
3. the file must contain one coding thing you haven't done before (aka something you learned today in this session)
4. submit your pull request including
    1. your code
    2. a description in the comment of the purpose of the code
    3. a figure you generated (optional)
    4. one thing you looked up after class that you were curious about
6. stick with it, your assignment isn't complete until I merge the PR, we will have discussions in the comments
  
  
# Footnotes
1. https://www.kdnuggets.com/2018/03/5-things-reinforcement-learning.html
2. https://en.wikipedia.org/wiki/KWL_table#:~:text=The%20letters%20KWL%20are%20an,methods%20of%20teaching%20and%20learning.
3. https://www.17lands.com/public_datasets
4. Extra Credit: This method is not optimized for R. It looks more like how someone would do it in old school python. For 25 points and the lead, refactor this code into a vectorized solution.
