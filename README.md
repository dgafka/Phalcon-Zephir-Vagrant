<h2> Virtual Machine For Zephir Extensions Development </h2>

<h4>Requirements:</h4>
1) VirtualBox
2) Vagrant


<h4>Installation</h4>
Clone repository "git clone git@github.com:dgafka/Phalcon-Zephir-Vagrant.git"
Inside Phalcon-Zephir-Vagrant folder run: "vagrant up"

<h4>Usage</h4>
If path your to vagrant file is: "/home/user/projects/phalcon-zephir-vagrant/",
Create folder "/home/user/projects/data/".
This folder will synchronized with "/vagrant_data/" folder inside virtual machine. 
Here you will be able to build extensions locally and compile them inside vagarant machine.

<h5>First extension</h5>
To build your first extension, log into vagrant via: "vagrant ssh" command.
Then "cd /vagrant_data"
Next: "zephir init utils". This will create your first extension project with all necessary stuff.
Now you're able to develop your extension exactly like the tutorial says: "http://zephir-lang.com/tutorial.html".
You will be able to do this in your local machine. The project is now visible inside "/home/user/projects/data/utils" (local).
When you're done run "zephir build", inside /vagrant_data/utils/ folder from your vm.
