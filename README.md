# public_test_repo

To add ssh on github:
1.  $ ssh-keygen -t ed25519 -C robertdegracia@gmail.com
-  creates the secret id_ed25519 and public id_ed25529.pub files

2.  $ eval "$(ssh-agent -s)"
- starts up the key agent

3.  $ vi ~/.ssh/config and enter:
- Host *
  AddKeysToAgent yes

4.  $ ssh add ~/.ssh/id_ed25519

5.  Add ed25529.pub content to github
- Go to git hub and Profile | settings | 'SSH and GPG Keys' | Press button
         'New SSH key' |  add contents from ed25529.pub 

6.  To test:  $ssh -T git@github.com
- Test connection to the git hub
    
7.  To clone as an example:
$ git clone git@github.com:robertdegracia/public_test_repo.git
