# A/B Testing - New Feature of Cookie Cats Game: Project Overview 
* Cookie Cats is a hugely popular mobile puzzle game developed by Tactile Entertainment. It's a classic "connect three" style puzzle game where the player must connect tiles of the same color in order to clear the board and win the level. It also features singing cats. We're not kidding!
* As players progress through the game they will encounter gates that force them to wait some time before they can progress or make an in-app purchase. In this project, we will analyze the result of an A/B test where the first gate in Cookie Cats was moved from level 30 to level 40. In particular, we will analyze the impact on player retention and game rounds.

## Code and Resources Used 
**Python Version:** 3.10  

**Packages:** scipy, pandas, numpy, matplotlib, seaborn, sklearn

**Dataset:** https://www.kaggle.com/code/ekrembayar/a-b-testing-step-by-step-hypothesis-testing/data

**Reference: https://www.kaggle.com/code/ekrembayar/a-b-testing-step-by-step-hypothesis-testing/notebook**

## EDA 

![alt text](https://github.com/ahnngo/AB-Testing-New-Feature-of-Cookie-Cats/blob/master/Before%20Removing%20The%20Extreme%20Value.png)

We will treat outliers by removing all sum_gamerounds value > 2640 and sum_gamerounds value == 0

![alt text](https://github.com/ahnngo/AB-Testing-New-Feature-of-Cookie-Cats/blob/master/After%20Removing%20The%20Extreme%20Value.png)
![alt text](https://github.com/ahnngo/AB-Testing-New-Feature-of-Cookie-Cats/blob/master/The%20number%20of%20users%20in%20the%20game%20rounds%20played.png)

There is a huge decrease in terms of retention as the difficulty of the game keeps increasing. This could be attributed to several reasons

* When the user reaches around round 150, the difficulty gets massively harder, making it more challenging for users to follow along
* There may be a trade-off between purchases and chance of moving to the next level, which means if the users do not purchase new functions/skins/skills, they will not likely to get through. This may help the producers have more financial benefits, but at the same time decrease users' retention to the game
* There is a novelty effect, which the users appear interested to the game at first, then their interest decreases overtime, which is expected

**We should work along with the User Experience Research Team to be able to figure out what happens to give out suitable solution**
 
## Conclusion

* In terms of difference of users' retention over game round, there is not statistical proof to conclude that changing the first gate from level 30 to level 40 would make any difference. I suggest game developers should run the test on a longer time to see more obvious results. If the test was run on a long enough period, then the result indicates that new feature does not really contribute as much, thus our A/B test is unsuccessful. 

* In terms of retention after 1 day and 7 days, there is also not enough statistical proof to conclude that new feature will keep users stay with the game longer. Both control and treatment group produce the similar mean with similar standard deviation. 
