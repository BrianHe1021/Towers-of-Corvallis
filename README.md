# Towers-of-Corvallis
Towers of Corvallis consist of 3 pegs and n disks. Unlike in Towers of Hanoi, here any disk can go on any other. The goal is to get from an initial position to a goal position in the smallest number of steps. Remember you can only remove the top disk from the peg at any time and place it on the top of the disks on another peg.

Let us number the disks 0-9 so that we can denote a state with 3 numbers or lists or arrays or whatever. For example, (0123456789,-,-) is a state and (012,3456,789) is another state, etc. The leftmost digit in the number indicates the top disk. Let us fix the goal (final) state to be (9876543210,_,_) if there are 10 disks (and similarly for n<10 disks). Also fix the initial state to be some configuration of disks, all of which are on the first peg. Call the three pegs A,B, and C.

Write a search program to solve this puzzle using A* and beam search. Note that A* is equivalent to beam search with beam width = infinity. Design and implement one admissible heuristic for this problem and one non-admissible heuristic.
 
       For each heuristic function h, 
         For beam widths 5, 10, 15, 20, 25, 50, 100, infty
           For at least 4 different sizes (number of disks)
             For each of the 20 problems p, 
		   Solve p using h or until NMAX nodes are expanded. 
                 Record data.
                       
A list of several problems with numbers of disks 4, 5, 6, 7, 8, 9, 10 are available. Only the starting state is described for each problem and all the disks are assumed to be on peg A. The final state for all problems is the same. It is to get all disks to peg A in the order 9876543210. The top disk is the leftmost. As described in the pseudocode, you should at least try 4 different sizes (number of disks) of problems.
