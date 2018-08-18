# g254app
a simple Grails 2.5.4 web application

cd ~/g2projects
grails create-app g254app
cd g254app
tree
grails dependency-report
grails integrate-with --git
git init
git add .
git commit -a -m "first commit"
git status
git remote add origin git@github.com:ashburndev/g254app.git
git push -u origin master

