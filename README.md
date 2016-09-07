# BigHalley

This is going to be great!


# Problem statement

We have a number of teams, each with a some workers within. They are moving
to a new building with many neighbourhoods. Given some weights between teams
how do we optimise where they sit?

## Simplifications
Within a neighbourhood we assume no distance between workers. So we should
never consider movements within a neighbourhood. The distance between workers
in different neighbourhoods is the taken as the distance between the centers
of the neighbourhoods. Distance is calculated as the dX + dY, we dont try and
go diagonally.

## Cost function
Sum(distance*weight) between all combinations of workers

## Toy example

6 Neighbourhoods, holding 20 workers each.
4 Teams with t1 = 50, t2 = 30, t3 = 20 and t4 = 10
Weights between teams:
t1,t3 = high
t1,t4 = low
t2,t3 = high
t3,t4 = low

Also people within team that are in different neighbourhoods has a
super high weight.
