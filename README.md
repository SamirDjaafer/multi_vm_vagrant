# Multi Virtual Machines

- 1 - First we configured our Vagrantfile to have 2 virtual machines running. We did this by adding another virtual machine inside of the `Vagrant.configure("2") do |config|` section
```Vagrantfile
config.vm.define "db" do |db|
    db.vm.box = "ubuntu/xenial64"
    db.vm.network "private_network", ip: "192.168.10.200"
    db.vm.provision "shell", path: "environment/db/provision.sh", privileged: false


  end
``` 

- 2 - Next we added a new provision script inside of the environment folder, we made a folder for db and put the provision shell script file in there.

- 3 - Next we needed an environment variable for DB_HOST so we set that in our provision.sh file for our APP, Why the app? Well our DB_HOST variable is set inside the app, if we set it in the DB shell script then the app does not know what DB_HOST is, which defeats the purpose of setting it. We can test it out first to make sure it works by SSH into the app and setting it in the ~/bash.rc file.

- 4 - Now we know what the DB_HOST is we can now npm start and connect to the db through our app.


- Jenkins Test!
- Jenkins Test !!
- Jenkins Test !!!jenkins test
- Jenkins Test !!!jenkins test
- Jenkins Test !!!jenkins test
- Jenkins Test !!!jenkins test
new test for jenkins again! 3 new commit again!!!!!!!!!
This should be visible on master if the build worked!!!!!!!!!!!!


Jenkins test from AWS!!!!!!!!!
Jenkins test !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

change
test
test
test
test
test
test
test
