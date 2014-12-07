<h2> Virtual Machine For Zephir Extension Development </h2>

<h4>Vagrant contains:</h4>
<ul>
  <li>Zephir language installed (accessible via 'zephir' commmand)</li>
  <li>Apache2 webserver installed</li>
  <li>Php ver. 5.4.35 </li>
  <li>Composer installed (accessible via 'composer' command)</li>
  <li>Phalcon2 extension added to PHP</li>
  <li>Synchronization with your local folder (read bellow)</li>
</ul>

<h4>Requirements:</h4>
1) VirtualBox<br/>
2) Vagrant<br/>


<h4>Installation</h4>
Clone repository "git clone git@github.com:dgafka/Phalcon-Zephir-Vagrant.git"<br/>
Inside Phalcon-Zephir-Vagrant folder run: "vagrant up"<br/>

<h4>Usage</h4>
If path your to vagrant file is: "/home/user/projects/phalcon-zephir-vagrant/",<br/>
Create folder "/home/user/projects/data/".<br/>
This folder will synchronized with "/vagrant_data/" folder inside virtual machine. <br/>
Here you will be able to build extensions locally and compile them inside vagarant machine.<br/>

<h5>First extension</h5>
To build your first extension, log into vagrant via: "vagrant ssh" command.<br/>
Then "cd /vagrant_data"<br/>
Next: "zephir init utils". This will create your first extension project with all necessary stuff.<br/>
Now you're able to develop your extension exactly like the tutorial says: "http://zephir-lang.com/tutorial.html".<br/>
You will be able to do this in your local machine. The project is now visible inside "/home/user/projects/data/utils" (local).<br/>
When you're done run "zephir build", inside /vagrant_data/utils/ folder from your vm.<br/>
