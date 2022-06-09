# Generating a new SSH key and adding it to the ssh-agent
#https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

ssh-keygen -t ed25519 -C "<git-hub-email>"
 
eval "$(ssh-agent -s)"
  
ssh-add ~/.ssh/id_ed25519
  
# Adding a new SSH key to your GitHub account  
# https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account
  
vim ./.ssh/id_ed25519.pub
  # copy contents to clipboard
  # add it to github  

  
# Switching remote URLs from HTTPS to SSH
# https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-https-to-ssh  
# cd into git dir
git remote -v
  
git remote set-url origin git@github.com:r1kemp/test_private.git
  
  
  
