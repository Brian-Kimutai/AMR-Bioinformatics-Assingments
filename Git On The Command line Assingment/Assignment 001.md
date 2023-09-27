## Quiz 1 

> 'On your github account, create a github repo named "Only alkanes"'
- To do this 

## Quiz 2

> Clone the newly created repo to your local machine,

- To clone a repository means to download or duplicate an existing Git repository into your local computer,
- To do this on the command line;
   - Open GitHub and go to the GitHub repository that you want to clone.
   - Click “Code” and copy the given URL. For this case the  URL is https://github.com/Brian-Kimutai/Only-Alkanes
   - Open the terminal and change the current working directory to the location where you want the cloned directory ; in this case "Only Alkanes"
     i.e
     ```
     cd Working-with-Git/Only-Alkanes/
     ```

   - In put the command ``git clone`` , paste the URL you copied earlier, and press “enter” to create your local clone.
   - i.e
     ```
     git clone https://github.com/Brian-Kimutai/Only-Alkanes
     ```

## Quiz 4

> Copy the contents of alkanes folder from shell-lesson-data/exercise-data/, used in previous classes, into your "Only alkanes" repo

- To do this;
   - Navigate to the Alkanes folder `` cd shell-lesson-data/exercise-data/alkanes ``
   - Copy the contents  of the Alkanes folder into the "Only Alkanes" repo. by inputing:
     ```
     cp *.txt *.pdb ~/Working-with-Git/Only-Alkanes/
     ```
     
## Quiz 5

> Run the following command while inside the repo for j in `ls *.pdb`; do for k in {1..100}; do cp $j $(basename -s .pdb $j)$k.pdb; done; done

. Input;
```
for j in `ls *.pdb`; do for k in {1..100}; do cp $j $(basename -s .pdb $j) $k.pdb; done; done
```


## Quiz 6

> Find the easiest way to push only the .pdb files whose number suffix is divisible by 10

##  Quiz 7

> Document your answer/work-around for the task number 5 in a markdown file named "Easiest solution.md"
