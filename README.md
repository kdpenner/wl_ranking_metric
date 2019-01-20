## The current ranking system
## 
At weightlifting competitions, men and women compete separately. Each
gender is further divided into bodyweight classes. Rankings are
determined within the gender and bodyweight categories by total amount
of weight lifted.

The categories exist because a female weighing 87 kg can lift more than
a female weighing 55 kg. The heavier female has more muscle mass than
the lighter female; the amount of weight a person can lift scales with
muscle mass. Furthermore, a male weighing 87 kg can lift more than a
female weighing 87 kg.

The categories must exist only if the ranking metric is total amount of
weight lifted.

## An inclusive ranking system
## 
Work done at the Alberta Weightlifting Association has resulted in
empirical functions used to calculate the maximum weight lifted as a
function of bodyweight. World record lifts establish these functions. (A
cautionary note: because world records change, so do these functions.)
The function for males is different from the function for females. The
following [notebook](./new_metric.ipynb) presents an exercise in using
two quantities for the ranking metric: 1) total (i.e., snatch + clean
and jerk) amount of weight lifted; and 2) the world record for the
athlete's gender and bodyweight.

Ranking by the ratio of total to maximum weight lifted obviates both
gender and bodyweight categories. Men and women can compete directly
(with the caveats shown below) and without regard to bodyweight.

For now, the functions defining the maximum weights require that the
athlete's gender is known. My hope is that one day a person
professionally studying these metrics will find a replacement variable
for gender.

## The new system applied to a competition
## 
I'm presenting a ranking based on the results of the 2018 IWF World
Championships. See the [Jupyter notebook](./new_metric.ipynb) for
detailed results and more information on existing ranking
inconsistencies among several gender and weight classes.

A few summary statistics for the top 20 lifters:

1) 5 are female and 15 are male.

2) The median bodyweight is 81 kg. The minimum bodyweight is 48 kg and
the maximum is 169 kg.

3) There are 9 `upsets'. There are 10 bodyweight classes for each of the
2 genders, meaning that, by the original metric of total weight lifted,
there are 20 first-place lifters. For the new metric, the top 20 lifters
are populated by 11 of the first-place lifters and 9 of the second- and
third-place lifters.

4) The cutoff `Sinclair fraction', or the ratio of total to maximum
weight lifted, is 0.9580.

5) Differences in the Sinclair fraction can be quite small. The first
and second lifters are separated by 0.0136, while the second and third
lifters are separated by 0.000064. Someone who studies ranking metrics
professionally should decide when to call these small differences a tie,
and what metric to resort to as a second ranking. (Perhaps ratio of
snatch to clean and jerk?)

## Problems with reproducing the original ranking system
## 
I tried to reproduce the rankings by the original metric. According to
IWF literature, ties are resolved by ranking by descending total weight
lifted, then by ascending clean and jerk (or, equivalently, by
descending snatch), then by ascending attempt number for the successful
clean and jerk. I found 20 inconsistencies. For example:

name, rank, gender, bodyweight class, c+j weight, attempt number

AL-HUSSEIN Ahmed Farooq Ghulam, 21.0, M, 81, 185.0, 2.0

GETTS Victor, 22.0, M, 81, 180.0, 1.0

QERIMAJ Erkand, 23.0, M, 81, 180.0, 1.0

All 3 lifters have the same total. My understanding of the literature is
that Getts and Qerimaj, who jerked less and snatched more than
Al-Hussein, should rank higher than Al-Hussein. Please follow up with me
[by email](mailto:kdpenner@gmail.com) if you know the solution to this
inconsistency.