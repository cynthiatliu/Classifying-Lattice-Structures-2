# Classifying-Lattice-Structures-2
Using a very meta predictor (a random forest that takes predictions from a random forest
which in itself takes predictions from its constituent trees) to try to predict the overarching
crystal structure for a crystal that contains planes at certain (h,k,l) combinations

#Details

This is some additional work on the all-structures problem, putting us closer to a fully automated and accurate solution.
The goal in this attempt was to see if, instead of trying to label individual points and achieve a plurality,
which does not work as once P is introduced every single point in the space fulfills at least 2 conditions,
we can make Python learn a pattern among the predictions themselves. For example, a crystal whose planes were
correctly labeled A, B, and C with each set containing two values of the same parity and one not could only be
one of I or P based on what the actual coordinates were.

It appears at first glance from the data that this method might work but not well. I will do statistical analysis soon.
Here were the resulting predictions:
[ 0.  0.  0.  0.  4.  2.  0.  1.  1.  3.  0.  0.  3.  3.  4.  0.  0.  5.
  2.  2.  5.  6.  0.  3.  0.  2.  1.  1.  0.  3.  2.  2.  5.  3.  2.  3.
  3.  2.  1.  1.  3.  6.  2.  5.  4.  1.  1.  1.  1.  3.  2.  5.  1.  2.
  4.  0.  1.  2.  5.  2.  2.  0.  0.  4.  2.  1.  2.  6.  1.  1.  3.  2.
  2.  1.  2.  5.  3.  6.  5.  1.  3.  3.  1.  5.  0.  1.  2.  3.  3.  0.
  1.  4.  0.  3.  3.  4.  3.  3.  6.  5.  4.  4.  6.  0.  0.  1.  2.  4.
  5.  5.  1.  6.  1.  4.  6.  4.  3.  5.  3.  6.  5.  2.  1.  3.  2.  4.
  5.  5.  6.  6.  0.  2.  1.  4.  5.  0.  2.  6.  0.  5.  5.  6.  5.  6.
  3.  2.  2.  2.  4.  5.  6.  1.  2.  3.  2.  3.  5.  3.  5.  6.  3.  5.
  6.  3.  6.  5.  2.  3.  5.  3.  5.  5.  0.  0.  3.]
  
  I = 0, F = 1, A = 2, B = 3, C = 4, R = 5, P = 6.
  The real answers were: the first 25 are 0's, next 25 are 1's, and so on and so forth.
