## Implementation
This is a dendropy-based implementation for a new idea of rooting a phylogenetic tree, called the minVar (MV) root. Our rooting method roots the tree at the point that minimizes the variance of the root to tip distances. The code was designed to be easily generalized for a class of 'optimization-based' rooting methods (some of which are under developing), which includes a fast version of the traditional midpoint (MP) rooting as well.

Complexity: the rooting methods are linear (with the number of species) in time and memory.

## Dependencies:
- python (version 2.7 recommended)
- dendropy (version 4.2.0 recommended)

## Usage:


- python FastRoot.py [-h] -i INPUT -m METHOD [-o OUTFILE] [-s SCHEMA]

  -h, --help            show help message and exit
  
  -i INPUT, --input INPUT:
                        input file
                        
  -m METHOD, --method METHOD
                        method: MP for midpoint and MV for minVAR
                        
  -o OUTFILE, --outfile OUTFILE
                        specify output file
                        
  -s SCHEMA, --schema SCHEMA
                        schema of your input treefile. Default is Newick



NOTE: FastRoot.py works with single tree only. 
To simultaneously root a list of trees (i.e. a list of gene trees), use FastRoot\_multi.sh. The options are the same as for FastRoot.py, but all options are required (sorry).   

The following scripts might be more handy but only work with single-tree input, and don't accept optional options.


- python MP\_reroot.py \<tree_file_in_newick\>

- python MV\_reroot.py \<tree_file_in_newick\>

## Output:
The FastRoot.py with -o will output to the specified destination. Without -o, it prints the tree to stdout. 
The MP\_reroot.py and MV\_reroot.py will place the output in the same directory as the input tree with suffix MP\_rooted or MV\_rooted accordingly.
