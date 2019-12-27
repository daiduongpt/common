### Git
---------------------------------------------------------------------------------

#Command line instructions
You can also upload existing files from your computer using the instructions below.


#Git global setup
git config --global user.name "Duong Dai Vu"
git config --global user.email "5147386-duongvu_boca@users.noreply.gitlab.com"

#Create a new repository
git clone git@gitlab.com:avistel/avicom.git
cd avicom
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master

#Push an existing folder
cd existing_folder
git init
git remote add origin git@gitlab.com:avistel/avicom.git
git add .
git commit -m "Initial commit"
git push -u origin master

#Push an existing Git repository
cd existing_repo
git remote rename origin old-origin
git remote add origin git@gitlab.com:avistel/avicom.git
git push -u origin --all
git push -u origin --tags
