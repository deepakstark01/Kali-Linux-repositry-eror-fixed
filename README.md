# Fix by Deepak
# Kali-Linux-repositry-eror-fixed
# follow these bash cmd in terminal

# Delete old keys by following cmds :
root@kali:/#  rm -rf /var/lib/apt/lists
root@kali:/#  apt-get update 
root@kali:/#  apt-get install kali-archive-keyring

# if above cmd is not work then gpg eror fix by these: 

root@kali:/#  gpg --keyserver pgpkeys.mit.edu --recv-key  ED444FF07D8D0BF6
root@kali:/#  apt-key adv --keyserver hkp://keys.gnupg.net --recv-keys 7D8D0BF6
root@kali:/#  gpg --keyserver hkp://keys.gnupg.net --recv-key 7D8D0BF6
root@kali:/#  gpg -a --export ED444FF07D8D0BF6 | sudo apt-key add -

root@kali:/#  apt-get update

# Thanks it's working better now.
