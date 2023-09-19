

> On your github account, create a github repo named "Only alkanes"

> Clone the newly created repo to your local machine

> Copy the contents of alkanes folder from shell-lesson-data/exercise-data/, used in previous classes, into your "Only alkanes" repo

> Run the following command while inside the repo for j in `ls *.pdb`; do for k in {1..100}; do cp $j $(basename -s .pdb $j)$k.pdb; done; done

> Find the easiest way to push only the .pdb files whose number suffix is divisible by 10

> Document your answer/work-around for the task number 5 in a markdown file named "Easiest solution.md"
