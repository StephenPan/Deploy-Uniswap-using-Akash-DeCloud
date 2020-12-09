Akash Week 2 Challenge 1 Process
The process is the same as last week, submit deployment and submit json. Use deploy-2-1.yaml to deploy akash on akash.

To note the version has been updated from r11 to r13, to enter akash versionto see the old version is to update it.

There are two ways to update, one is to cut to the akash source folder, pull the new code and remake

cd $GOPATH/src/github.com/ovrclk/akash
git pull origin v0.9.0-rc13
make deps-install
make install
The other is to download the official compilation directly

wget https://github.com/ovrclk/akash/releases/download/v0.9.0-rc13/akash_0.9.0-rc13_linux_amd64.zip
sudo apt install unzip
unzip akash_0.9.0-rc13_linux_amd64.zip
mv akash_0.9.0-rc13_linux_amd64/akash go/bin/akash
The Mac update method is brew upgrade akash-edge

After the update is complete with akash versionconfirmation

The rest of the steps are the same as the first week. Generate json and submit it to the ecosystem library, just submit a pull request. Refer to the Akash Challenge 1 process (completed)

In the ecosystem library, you may need to merge the source remote branch first when pushing, you can use the following command: add the source master branch, pull it to the local master, and then merge the master

git remote add source https://github.com/ovrclk/ecosystem.git
git fetch source master
git merge source/master