pong ball - 90%
players - 5% player
borders
power ups
breakable obstacles - geometric shapes

#Components
- math logic
- server logic
- client logic - 50%
- javascript
- nodejs
- express
- assets
- for the assets we can just make a line using javascript paint
- mouse input -
- do we have a border
- sound effects
- other players

#Offensive Powerups
- adjustable axis paddle
- Deathball - destroys the paddle of the next person which touches the ball
obstacles -
- Shrink paddle
- Fireball - rips a hole through the net
- Laser Paddle - fires lasers that if hit the ball changes its trajectory
- Topspin
- Backspin
- Cut n Paste - Steal someone elses powerup, upon activation ball freezes and allows player to select one of the other player's powerups, maybe just get 4 random powerups from the players, and you push up down left or right, or selects at random from the available powerups stored in somebodies array

#Defensive Powerups
- Invulnerability/Immunity
- Grow Paddle
- Sticky paddle
- Safety Net

#Neutral Powerups
- ShadowBall - ball that you an't actually hit, the paddles won't hit it, but follows rules of the other elements, doesn't , requires multiball, one extra ball, bounces off walls, hits obstacles, destroys powerups
- shrink & enlarge board
- multiball
- shadow multiball - half the balls are shadows, others
- Accelerate Ball
- Speed ball
- Black Hole - three black holes appear when powerup activated, all disappear after certain duration
- Freeze Ball - freezes for one second

#Future Idea
- Adjustable axis paddle

#How to create the poloygons
- Given an area and a point how do you draw the pentagon? Well, the number of angles between the sides needs to add up to 360 degrees.
- http://www.calculatorsoup.com/calculators/geometry-plane/polygon.php it looks like I'll be able to follow this logic for constructing the sides.

#How to look at collision detection in a non linear fashion.
- Originally I was making the collision detection only work for geometric rectangles that have borders of only real x,y coordinates. But when you rotate a geometric shape to no longer have its sides only on real x,y coordinates you need to detect collision in a different way. One way that If found was by computing the area by making 4 triangles between the point of collision and the four corners. Compute the area of each triangle. If the area between among the 4 triangles equals the area of the actual rectangle than there is a collision. If the area is less or greater than the area among the triangles then the point is not within the geometric shape. I feel like there must be a less computational way...

Upon collision find the distance from the center, and then based on rotation point find the nearest wall. then point the pong ball back at the center


Given 560, 700 and 580, 760 calculate the slope

Rise over Run, 760-700 = 60
580 - 560 = 20

60/20 = 6/2 = 3

Given x = 560 and y = 700 calculate x using 700 = 3 * 560 + x

-980 so the function of this line is f(x) = 3x - 980

Given x = 580 solve for y

Solve for tangent line by finding the midpoint

(560 + 580) / 2, (700 + 760) / 2

1140 / 2, 1460 / 2
570, 730

f(x) = -1/3x

Given a point, 4 faces, and a direction is it possible to determine which face gets hit first? given a positive slope you can know that the the point hit first is the lesser x, given a negative slope you know that the first hit is the greater x, given a positive slope when x's are equal

given a point find the two points where the new x and y should be
x2 + y2 = d2
