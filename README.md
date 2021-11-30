# Medieval-Battle
 This is a medieval battle game implemented in Haskell based on brick.

## Setting

The basic setup of this game is to allow two players to play as a hero on a battlefield against each other. Heros can move freely on the ground but should stop when it encounters an obstacle. Heros can fire forwards in a straight line and eventually hit an obstacle or the enemy. Players that are hit will lose a certain amount of life. If the player lose all the life points, the player will lose.

We first designed three heros in the game: Archer, Witch, Assassin. Archer's attack has more damage but requires longer intervals. Oppositely, Assassin's attack has less damage but is quick to cool down. Witch does not cause frequent or huge damage, but can gradually heal up herself with the magic.


## Goal
We are using haskell language to see if functional programming has its unique advantages when implementing some very common small software. We initially use brick as the base framework for our project. If is possible, we will try to implement more fancy features in the game by exploring other libraries in the hackage ecosystem.


In addition to some pursuits beyond programming, we also hope to seek some innovative ideas. For example, we may make slight changes to the gameplay and rules to make the game more paced and competitive, like more heros or giving them unique talents. We may also try to implement cooler explosion effects or smoother operation design to enhance the player's interaction experience.

## Contributors
Jiangjian Guo :StereoNy

Hansong Zhang :zhs1397

Shicheng Bei :LaurensBeYoung

Zihao Wang :wang-zao




# Milestone
updated: 11/30/2021

## Structure

If we need to achieve our game goals, we first need to be very clear about the design of the components and how they interact with each other. In general, I think our project could perhaps contain the following components.

![image](https://user-images.githubusercontent.com/57669165/143992633-6981e595-80b8-4f28-b092-3abbed4d3ee2.png)



In general, it seems that these three components will be the main structure of our project. the UI part is mainly the basic visual display base and the presentational content that interacts closely with the user. the Object includes all the elements that may have multiple states in the game, and we need to make it a relatively cohesive thing, so that they have to be easily reusable, act according to their own logic, record and change states. Controllers include something that dispatches and controls Objects at a macro level, and feeds visual changes caused by changes in the relationship between Objects to the UI layer for updates in a timely manner. In short, Controllers make the game run.


## Challenges

We currently split up the work to try to build different modules. We managed to build some simple GUIs based on our understanding of the Brick framework, which allowed us to perhaps improve it further in the direction we had in mind. We also implemented some basic logic for simple blocks to collide with each other and detect positions, which will later have their own unique properties and develop into obstacles and different characters.
The biggest challenge we've encountered so far comes from the Controller section. We seem to be able to successfully reference the contents of the other two sections in a master file and read their state and information. But the problem is that our physical engine seems to do a lot of the work. For example, we are now just using a board to simulate a two-dimensional physical space, but we seem to need speed, direction, distance, collision detection, and a host of other functional modules. These things are implemented one by one indeed seems to be doable, but we go to the progress is currently very limited.
In addition, because there are some features are required to wait until some of the basic elements are ready to start further development, such as allowing player input monitoring manipulation of object movement and shooting seems to be the Controller thing, but it needs Object in advance to build a good target of these capabilities. Therefore, on the one hand, we estimate that we will encounter some new challenges in the future, on the other hand, we must also learn how to be able to work more effectively as a team, so as to avoid the situation of waiting for each other.

## Objectives
We want to focus on solving the problems we encountered intensively in the near future. We hope to have the game basically in one piece by December 3rd, and it should be mostly functional by December 5th, with some difficult areas completely wrapped up and some successful testing and bug fixes by December 8th.

## Adjustments

If we don't accomplish our goals as expected, we may need to adjust our expectations for the game. I think there are two ways we can do this.
1. adjust the technical path. As soon as time allows, if an attempt doesn't work, then we might want to think about whether there is something wrong with the design of the module itself, such as it has unrealistic expectations, rather than our partner's lack of coding skills. We will try to use all the information available to us to try to solve the problem and clarify what we can do. We can adjust the technical route to make the overall game process uninterrupted. 
2. adjust the game design. Although in our vision, this design may not be too problematic, we do not have 100% experience and certainty. For example, in a two-player single-player game, we may be good at handling a single input, but if there are two inputs at the same time, or if two inputs that should be consecutive are interleaved, how should we ensure the validity of the input? Although we haven't encountered such a problem yet, this is indeed a frequent situation in two-player games. So if as a last resort, we might also simplify the game design, for example by turning it into a single-player game. The design of any functional module is expected to be adjustable in theory. It's just that we also have to strike a good balance, trying to reach our goals on the one hand, but also knowing how to give up when it doesn't work on the other. Sometimes, letting go is also a kind of deep love.

