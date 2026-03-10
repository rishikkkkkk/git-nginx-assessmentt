## Q1. What is the difference between git revert and git reset --hard? When would you choose one over the other, especially in a shared/team repository? 
git revert creates a new commit that reverses the changes of a previous commit, keeping the commit history intact.
git reset --hard moves the branch back to an earlier commit and permanently removes all commits and changes after it, rewriting the history.
reset in my local repo and revert in team/org repo

## Q2. Explain the three areas of Git (Working Directory, Staging Area, Repository). What happens to a file at each stage when you run git add and git commit? 
working dir - area or folder where ican edit or create files.
staging area - area where temporary changes or pre commit .
repository area - where all commits are saved and stored.

## Q3. What is a merge conflict and what causes it? Describe the steps you take to resolve one, referencing the conflict markers Git inserts into files. 

merge conflict is a conflict which occurs during merging two branches. it is caused generally due to the modification of same part of the same file.
to slove it in team we have to discuss with the other dev that thsi changes are good after finialising one we can slove it
conflict markers 
#### <<<<<<<< HEAD
#### =========
#### >>>>>>>>>> branch-name

## Q4. What is the purpose of the .gitignore file? Give two examples of file types or directories commonly ignored in a Python or Node.js project and explain why. 
gitignore file basically tell git to ignore the files or packages which are mentioned in it.

## Q5. Describe the difference between git merge and git rebase. What is the main advantage of rebase in terms of commit history, and when should you avoid using rebase? 
git merge combines changes from one branch into another whereas git rebase moves and reapplies changes from one branch to another.
rebase helps in making git commit history clean and liner.

## Q6. Explain NGINX's event-driven architecture. How does it differ from Apache's thread-per-connection model, and why does this matter for high-concurrency workloads? 
nginx uses event driven architecture where small no. of worker_processess hadle many connections at the same time instead of creating new thread for every request.

## Q7. What is the difference between sites-available and sites-enabled in NGINX? Why is the symlink approach used instead of putting all configs directly in sites-enabled? 
sites-available is the directory which stores all the config. files for diff websites like port no., location etc
whereas sites-enabled stores all the symlink created files for that websites that are going to be used by nginx.
it is easy to use symlink approach as it is easy to create , modify the config files rather than deleting and recreating it each time.
## Q8. What is a reverse proxy and why would you place NGINX in front of a Node.js or Python application running in Docker? What problem does it solve compared to exposing the app directly on port 80? 
reverse proxy is a server which is used to redirect the users to the appropirate application that they need.
because nginx acts as load balancer also , it handles incoming as well as outgoing traffic.

## Q9. Explain what SSL termination means in the context of a load balancer. What are the advantages over SSL passthrough? Where is the certificate installed in each approach? 
SSL termination means the load balancer decrypts the HTTPS trafic from the client, processes it, and then forwards the request to the backend server.
it helps in traffic inspection , routing and in load balancing also.


## Q10. What does the try_files $uri $uri/ =404 directive do inside a location block? Walk through what NGINX checks at each stage of that directive for a request to /about. 
it checks that the particular files exists or not. if it not exist it gives 404 error.

404 is a not found error.
