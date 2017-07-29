This is a fix for Vagrant, an annoying one for me at least, some people may not have it. 

I'll run <pre>vagrant up ubuntu/trusty64 --provider virtualbox</pre>

The error I'll get is <pre>The machine with the name 'ubuntu/trusty64' was not found configured for this Vagrant environment.</pre>

The fix: 

<pre>vagrant box add ubuntu/trusty64
rm Vagrantfile
vagrant init ubuntu/trusty64
vagrant up</pre> 
