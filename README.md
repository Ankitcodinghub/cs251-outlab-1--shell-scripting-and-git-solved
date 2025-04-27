# cs251-outlab-1--shell-scripting-and-git-solved
**TO GET THIS SOLUTION VISIT:** [CS251 Outlab 1- Shell scripting and git Solved](https://www.ankitcodinghub.com/product/cs251-outlab-1-shell-scripting-and-git-100-points-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;121082&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS251 Outlab 1- Shell scripting and git Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
This Outlab is to be done in pairs, unless we’ve informed you that you’re an exception. Pairing info here. Make sure you read the instructions at the end before submitting.

Task 1: BASH. Make An Autograder! (55 points)

For those of you who want a pointer to get started with bash scripting, this is nice.

In this task, we will familiarise ourselves with the UNIX command line, and explore how scripts can help us automate some useful tasks. Your code for this task will also be evaluated by a script, so please be careful and follow the naming conventions we specify.

Automated grading is something you’ll see more than once, and hopefully, doing this assignment will really show you why everyone insists that you be disciplined while naming your files.

We take a small example to explain the directory structure at each step (you can use the tree command to verify). We start with:

.

|– download.sh |– evaluate.sh `– organise.sh

Part 1: download.sh (wget, basename) (10 points)

(https://www.cse.iitb.ac.in/~vahanwala/ssl21/big_mock_case/) click the link to check. You need to write a script, download.sh, that is invoked as follows:

# bash download.sh &lt;link to directory&gt; &lt;cut-dirs argument&gt;

First notice that this script needs two command line arguments to work as intended. Thus, it should first check that it has been supplied exactly two command line arguments before proceeding further. If the check fails, it should print the following line (without quotes):

“Usage: bash download.sh &lt;link to directory&gt; &lt;cut-dirs argument&gt;” and exit with code 1.

Use wget in the quiet mode for this task. It is clear that you want to use the recursive option, and you do not want to download stuff from parent directories. If you don’t specify anything further, you’ll see that the downloaded directory you actually want is nested in directories, starting from the one corresponding to the host, eg. www.cse.iitb.ac.in, within that ~vahanwala, within that ssl21 and finally within that is the directory you actually need.

wget has an option for not creating a directory corresponding to the host, but even if you invoke that, you’re still stuck with 2 levels of nesting that you don’t really want. That is where the cut-dirs flag will help. You don’t need to worry about your script being fed the wrong argument for this.

At this point, the directory structure should look something like (assume that inputs, outputs, submissions do not have any further subdirectories):

.

|– download.sh |– evaluate.sh

|– mock_grading

| |– inputs

| | |– 0.in

| | `– 1.in

| |– outputs

| | |– 0.out | | `– 1.out | |– roll_list

| `– submissions

| |– 180070026bar.cpp

| |– 180070035.cpp

| `– 180070035foo.txt

`– organise.sh

Note: The cut-dirs parameter will be specified in such a way that just the wget command will save the downloaded directory locally with the same name as the remote one. Eg. in this example, it will be 2.

Part 2: organise.sh (ln, for) (20 points)

Alright! You now have the roll list of students, the stuff they have turned in, the inputs to test their code, and the expected output corresponding to each input.

There’s a small problem though. If you look in the submissions directory, you’ll find that everyone’s files are together. If you run code from here, it might just so happen that Bob’s .cpp file finds Alice’s .h file particularly helpful. Thankfully, the files are named honestly: every file begins with the roll number of the student who submitted it, and we assume that all roll numbers are of equal length.

Our organise.sh will be called as follows:

# bash organise.sh

On running, it should create a directory called organised under the same directory as the scripts. Within the organised directory, it should create directories named after every roll number, eg. 180070026/, 180070035/, … (see roll_list under the mock_grading directory for the complete list of roll numbers)

For example, if roll number 180070035 has submitted 180070035.cpp, then in organised/180070035, the file 180070035.cpp is a symbolic link that’ll point to ../../mock_grading/submissions/180070035.cpp

Make sure you use relative paths while creating the symbolic links.

Now, the directory structure should look like:

.

|– download.sh |– evaluate.sh

|– mock_grading

| |– inputs

| | |– 0.in

| | `– 1.in

| |– outputs

| | |– 0.out | | `– 1.out | |– roll_list

| `– submissions

| |– 180070026bar.cpp | |– 180070035.cpp | `– 180070035foo.txt

|– organise.sh

`– organised

|– 180070026

| `– 180070026bar.cpp -&gt; ../../mock_grading/submissions/180070026bar.cpp

`– 180070035

|– 180070035.cpp -&gt; ../../mock_grading/submissions/180070035.cpp

`– 180070035foo.txt -&gt; ../../mock_grading/submissions/180070035foo.txt

For simplicity, you can assume that everyone who is on the roll-list has submitted at least one file and at most one cpp file.

Part 3: evaluate.sh (g++, diff, timeout, redirection, sort) (25 points)

We are now ready to do the actual grading. You can assume that each student has submitted at most one .cpp file; these are the only files we care about in this step. We will run this script as

# bash evaluate.sh

On running, this script will generate two files: marksheet.csv and distribution.txt. These, as usual, will be in the same directory as our three scripts. Each of these files will have as many lines as there are students, i.e. roll numbers in roll_list.

marksheet.csv will have the score of students, sorted in lexicographical order of roll numbers, in the format: &lt;roll number&gt;,&lt;score&gt; on each line. For example:

180070035,2

distribution.txt will have just the scores, one on each line, sorted in descending order of the integer score.

How are these scores calculated though?

Suppress the error messages with 2&gt;/dev/null (2 refers to stderr which is, as it suggests, the standard file descriptor to which error messages are written, and what we do here is suppress stuff by redirecting it to a null device)

Now, the inputs and outputs in mock_grading come into play. For each input mock_grading/inputs/foo.in, the expected output is in mock_grading/outputs/foo.out

You’ll have to do something like

# ./executable &lt; input &gt; output

The nice thing here is that the input file will of course exist, and the output file will be generated regardless of whether executable actually exists. Try it yourself!

But be careful! This is student code, there can be errors like segmentation faults, so you also need to redirect error messages to /dev/null just like you did while compiling. There’s one more catch: you can’t let code run forever, so set a timeout of 5 seconds for running each testcase. For convenience, please also suppress Segfault error messages by piping to the null command.

For each testcase, compare the generated output with the expected output. If they are exactly the same, add 1 to the student’s score, else, do nothing. Don’t worry, we will only test you on cases where the expected output is not blank.

Thus, you populate marksheet.csv as you evaluate each test case for each student. From here, making distribution.txt won’t be too hard.

Here’s what your working directory will look like, finally: (in this instance, it so happened that 180070026bar.cpp threw a compiler error) From the diagram, it should be clear that you’re doing the compilation and testing from within organised/&lt;roll_no&gt;

Disclaimer: Suppressing error messages is just a hack that is sometimes handy. For other applications, it is usually a bad idea.

.

|– distribution.txt |– download.sh |– evaluate.sh

|– marksheet.csv

|– mock_grading

| |– inputs

| | |– 0.in

| | `– 1.in

| |– outputs

| | |– 0.out | | `– 1.out | |– roll_list

| `– submissions

| |– 180070026bar.cpp | |– 180070035.cpp

| `– 180070035foo.txt

|– organise.sh

`– organised

|– 180070026

| |– 180070026bar.cpp -&gt; ../../mock_grading/submissions/180070026bar.cpp

| `– student_outputs

| |– 0.out

| `– 1.out

`– 180070035

|– 180070035.cpp -&gt; ../../mock_grading/submissions/180070035.cpp

|– 180070035foo.txt -&gt; ../../mock_grading/submissions/180070035foo.txt

|– executable

`– student_outputs

|– 0.out `– 1.out

Task 2: Git (45 points)

In this task we will get you acquainted with git.

Git is a VCS (Version Control System) that lets you easily manage several versions of your code and collaborate with your teammates, no matter how small or large your code base is.

You can manage your work locally in a Git repository, or “push” your work to a remote server such as the widely used GitHub or our own IITB CSE GitLab. Moreover, you can connect your local repo with the remote repo to sync the changes. Connecting to the same remote repo allows your teammates to see all the changes that you “push” to the remote repo. If granted permission, your teammates too can push their changes to the code to your remote repo, which basically allows you to collaborate with your teammates.

Although you will have to submit most of your assignments through Moodle, we suggest that you start using git right away to collaborate with your teammates, it will make your life much easier later.

Let’s get you started!

Sub Task 1: (15 points)

(checkout, add, commit, push, pull, branch, merge, rebase)

Note: The person with the lexicographically smaller roll number is referred to as ‘you’ and the other one as ‘your friend’

You and your friend are working as freelancers and your client requires you to implement the backend for their app’s login page.

Part 1: First Commit (You) (2 points)

1. Create a private repository on IITb CSE Git Server from ‘your’ account. Name the repository as &lt;first-rollno&gt;-&lt;second-rollno&gt;-git (if this name is not available add random extra digits at the end: &lt;first-rollno&gt;-&lt;second-rollno&gt;-git42 )

Update: In case any member of your team does not have a CSE Ldap, you can create a private repo on GitHub. Make sure the github accounts are created from your IITB Ldaps, i.e. your iitb email ending with @iitb.ac.in

Use your regular email account for github. Make sure it’s reasonably clear who you are from your id. (updated in light of recent email from head CC)

If, for whatever reason, you can’t use CSE git (no CSE LDAP, login doing weird stuff, fill this form and proceed with GitHub as described above)

2. Add ‘your friend’ as a collaborator

The following steps are to be performed by the ‘you’: (git clone, git add, git commit, git push)

1. Download passwords.h from moodle. Create a file called utils.h. Implement a function with the following signature in it (don’t forget to include passwords.h in it):

bool login(string name, string password)

This function returns true only if a user with the given name is present in the database(which is defined in passwords.h) and the password matches. Use auxiliary functions defined in passwords.h to complete this function.

2. Create a main.cpp that takes in two strings from stdin, a name and a password.

Call the function login from main. If it returns true, print Success! else print Login Failed 🙁

3. Now add all the changes in your working directory to the staging area (git add) and commit these changes with the commit message feat: Login API

Learning:

This will create a master branch and your first commit in git. A commit is like a snapshot of your work. If you make any changes to your working directory or create any new commits, you can always come back to any previously created commit and checkout what you were up to when you made that commit.

At its heart git is just a content-addressable filesystem, i.e. it stores files for you and you can retrieve any file, anytime, based on the content of that file. For doing that git internally calculates a hash for your file, and you can retrieve that file later by remembering the hash that git gives you. However, we don’t do this dirty work ourselves. Git provides us with a nice set of user-friendly commands that hide away these details and make our lives easier.

Now, use the command git log to see the history of commits that you have made. You will only see a single commit, showing a string of 40 characters, saying that your current HEAD is at master, as follows:

Git stores everything and anything that you throw at it(even your commits) in its content-addressable filesystem. Using this 40 character hash value, you can refer to any commit you have made. However, it’s a pain to remember these long hash values when your project is very big. For this, git provides us with objects called refs.

Basically, git lets you attach names to some important commits / milestones in your project. So, to return/refer to a previous commit you can simply use this name. Several types of refs are available in git, the most frequently used are: tags and branches, and they behave differently.

Branch: Apart from other metadata, like the author, time, etc. for a commit, git also stores pointers to the commits that immediately came before it. A branch in a git is a movable pointer. As you make more commits on the current branch, this pointer moves forward and points to the latest commit.

Tag: a tag, as opposed to a branch, is a static pointer, mostly used as a milestone to refer to important updates or mark different versions of your code.

All the files, log and git objects are stored inside .git folder inside the repo.

4. Create a file README.md. And report the hash of the last commit that you made in it. Add this file to your staging area and create a new commit with the message

Adding README.

5. Push your commits to the remote branch master (git push)

Part 2: Branch off (Your Friend) (3 points)

Your friend needs to perform the following steps:

2. Create a branch named thisisabetteridea. And switch to this branch.

3. Download the file new_passwords.h from moodle and copy its contents to passwords.h in your current working directory.

5. Add changes to the staging area and commit your work with the commit message feat: The Better Idea

6. Push your commit to the remote branch thisisabetteridea

Part 3: Fixes (You) (2 points)

Your client is complaining that their users are confused and don’t know what to do when they land on the login page. You realize that you forgot to prompt users asking for their names and passwords.

You need to do the following:

1. Change the main function in main.cpp, ask the user to Enter Name: and Enter Password: before reading the two strings from stdin.

2. Add your changes to the staging area and commit your work with the commit message Fix: Adding Login Prompts

3. Push your commits to the remote branch master

Part 4: Rebase / Merge (Your Friend) (4 points)

Your friend finds out that you have made changes to the master branch after they branched off. Now, to test their code, your friend needs all the changes you made in their branch as well.

Your Friend can do one of the following things: (git rebase, git merge)

Rebase:

Rebase their branch (thisisabetteridea) to your master branch.

For this your friend needs to:

1. Checkout to their branch thisisabetteridea

2. Use the appropriate git command to rebase to your master branch

3. Resolve conflicts if any and continue to rebase if needed

(git rebase –continue)

4. Push their latest commits to the remote branch thisisabetteridea

OR

Merge:

Merge your master branch into their branch thisisabetteridea

For this your friend needs to:

1. Checkout their branch thisisabetteridea

2. Use the appropriate git command to merge your master branch into thisisabetteridea

3. Resolve Merge Conflicts if any and commit the changes with the appropriate commit message

4. Push their latest commits to the remote branch thisisabetteridea

Part 5: (You) (4 points)

After your friend implements the POC, you finally agree to agree. Now, you need to merge all their work into your master branch which you are using to deploy the login page.

For this, you need to do the following things:

1. Checkout your master branch

2. Use the appropriate commands to merge his thisisabetteridea branch into your master branch.

3. Push your latest commits to the remote master branch

That’s it, you completed the basic login page your client asked for. Onward to more challenging tasks.

Sub Task 2: Saving Private Creds (30 points)

This task can be done by you or your friend or both.

This task is small (4-5 different commands) but tricky.

For this task you will need to download git-task2.zip provided to you on moodle.

This time a client asked you to handle the backend for their website and take care of their server. The previous developers who worked on the project were careless and added sensitive server credentials somewhere way back in the git history. You cannot publish your repo with such sensitive data exposed. Anybody could hack into your client’s backend.

You need to find out where (the commit) the server credentials (file creds.env) were added to the repo and remove this file from the entire git history to publish the repo. You will fix the repo that we gave to you and submit it back to us.

Note that simply deleting that file from your master branch and creating a new commit won’t be enough. Because then anyone can checkout one of your previous commits and still find out the server credentials.

Moreover, you cannot create a new repo by simply copying everything from master branch except creds.env because this repo is marked with important milestones (tags) and contains several versions of your server, which your client might need.

Evaluation Scheme:

● If I can’t find creds.env from the latest commit of the master branch, but I am able to retrieve it by checking out previous commits of master, with least damage done to the master branch history – 5 points

● If I can’t retrieve creds.env from the master branch, with the least damage to rest of the history – 15 points

● If I can’t retrieve creds.env from anywhere in the repo using any of the following commands: git log –reflog and git checkout from anywhere inside your rep, with the least damage done to the rest of the history – 30 points

(With git log/git show, trace the commit(call it commit X) that added creds.env. Branch off from the previous commit. Restore all files from commit X in the current working directory. Add only the required files to the staging area and create a commit(could use .gitignore here). Rebase the master branch from the commit X onto the newly created commit. Use git reflog to remove dangling(unreachable) commits from reflog, then use ‘git gc’ to prune history . You might find the following commands useful – checkout, branch, restore, rebase –onto, git reflog expire, git gc)

If you use the approach specified in the hint, when you use git log you will see only one commit with your username, rest all should be from the user guitarhero22

Do not create a new repo and artificially recreate the history. We will find out if you did so.

Notes:

● Hints are given in (this) form. If you find any commands in these hints find out how to use them and what they do, and then solve the problem

● This Guide has everything you need to know about Git. If you don’t understand something that I’ve said in this assignment or you want to learn more, you can read up on that particular topic from here.

Submission Instructions:

Bash:

Your submissions for Bash will be autograded, so please adhere to the naming conventions strictly. For your submission, first make a directory called &lt;rollno1&gt;-&lt;rollno2&gt; where rollno1 is the lexicographically smaller roll number. Eg. 180070026-180070035

The following should be the structure of your directory. Check with tree -a .

|– code

| |– download.sh | |– evaluate.sh

| `– organise.sh `– references.txt

Compress this &lt;rollno1&gt;-&lt;rollno2&gt; directory, strictly with the command tar -czvf. For example,

tar -czvf 180070026-180070035.tar.gz 180070026-180070035/

Git:

We will manually grade your submissions for Git.

Sub Task1:

Add users rushabh (for the time being) to your IITb CSE Git Server Repo.

Update:

IF you have a member who does not have a CSE Ldap, then create a private repo on github, and add the github user guitarhero22 as a collaborator.

Sub Task2:

Create a file report.txt which contains the commands that you used to solve the problem. And explain why you used a particular command. Before submitting please check with ls -a that .git is present in git-task2

Create the submission directory as that looks like this:

&lt;rollno1&gt;-&lt;rollno2&gt;

|– git-task2

`– report.txt

Compress this directory with the following command:

tar -czvf &lt;rollno1&gt;-&lt;rollno2&gt;-gt2.tar.gz &lt;rollno1&gt;-&lt;rollno2&gt;-gt2/ tar -czvf &lt;rollno1&gt;-&lt;rollno2&gt;.tar.gz &lt;rollno1&gt;-&lt;rollno2&gt;/

For BASH, since it is autograded, please make sure that you test your code by running it from within your Docker environment. If you use Windows, there might be an issue with the newline character, so you could use an editor like vim on the Docker command line. In any case, please check on Docker before submitting!

For some scripts, if you use Windows, you might see an error like “ : Command not found” when you try to run stuff on Docker. This is because Windows and Unix encode newlines in text files differently: it’s “ ” for Windows, and “ ” for Unix. Simply running dos2unix &lt;filename&gt; should fix the issue, and we will be mindful of this while grading. You can apt-get install dos2unix

Dear Rushabh,

Times New Roman is way classier than Arial.

Sincerely,

Mihir
