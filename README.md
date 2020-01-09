# Radar Final Project README

## Implementation steps for the 2D CFAR process:
* Define  number of Training cells for each dimension Tr and Td. Similarly, pick the number of guard cells Gr and Gd.
* By using 4 nested for loops (Two to loope on the whole grid and the other two to loop through the training cells around each CUT)
    ![RDM](image8.png)
* For each cell make sure that it belongs to the training cells not the guard cells. if so add it to the threshold. 
* Average the threshold by dividing on the number of training cells `(2Tr+2Gr+1)(2Td+2Gd+1) - (2Gr+1)(2Gd+1) `
* If the CUT level > threshold assign it a value of 1, else equate it to 0.
## Selection of Training, Guard cells and offset.
The Selection of the the algorithm pramaters were done using trial and error approach giving the groundtrouth on the initial position. 

## Steps taken to suppress the non-thresholded cells at the edges.

* By looping on the entire RDM we can check each cell if it's not equal 0 or 1, then it's non-thresholded cell so we set it to 0