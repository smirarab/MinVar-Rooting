# MP_reroot
This is a fast implementation of the midpoint rerooting. The code was designed to be reusable for implementation of a new idea of rerooting, called the minVar reroot, which reroots the tree at the point that minimizes the variance of the root to tip distances.

Complexity: both rerooting methods are linear (with the number of tips) in time and memory.

Dependencies:
- python (version 2.7 recommended)
- dendropy 4

Usage:

python MP_reroot.py \<tree_file_in_newick\>

python minVAR_reroot.py \<tree_file_in_newick\>

Output:
In the same directory as the input tree you will find the (re)rooted tree with the same name as the input with suffix MP_rooted or minVAR_rooted added.
