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