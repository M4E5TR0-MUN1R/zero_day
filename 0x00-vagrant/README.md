<div class="gap formatted-content">
<h2>Why use Virtual Machines? And why Vagrant?</h2>

<p>We’re glad that you’re adapting to the Framework! <strong>Always ask why!</strong><br>
It is important to ask yoursef: <em>“Why am I not just developing on my computer? I have all the tools I need!”.</em></p>

<h3>My machine vs. virtual environments</h3>

<p>Your computer’s environment - whether it’s Windows, MacOS or a Linux distribution - will change a lot over time, with or without you noticing. You will install applications, games, tools, … that will require and install different dependencies and at the end of the day you can end up having completely different behaviors or even have something not work because of software conflicts.</p>

<p>We won’t go into the details of Virtual Machines, but as their name tells, they are Virtual “Computers” that will emulate everything from the CPU to the RAM and Disk. Virtual Machines in the context of development are a means to <strong>isolate and maintain a stable environment</strong> that will basically <strong>run the same way on any host</strong> (any computer). This way, you can have any software installed on your Windows, MacOS, or whatever Linux distribution; your Virtual Machine will run its own environment, have its own programs, with their own versions, etc.</p>

<p>Using virtual environments prevents developers from saying <strong>“I don’t understand, it works on my machine …”</strong>. Here at School, we want to make sure that you have access to the same environment that will be used to correct your work (the Checker).</p>

<h3>The tools</h3>

<p>There are multiple tools out there that can help you create and manage virtual environments (notice that we use the term “virtual environment” here, as such environemnt is not necessarily a VM. Technologies using containerization allow one to manage virtual environments as well).<br>
We are using two tools at school: <strong>VirtualBox</strong> and <strong>Vagrant</strong>.</p>

<p><strong>VirtualBox</strong> is a Virtual Machine provider. The virtual machines themselves will be spawned using VirtualBox. VirtualBox is free and lightweight, which make it a perfect choice for us.</p>

<p><strong>Vagrant</strong> is a tool that sits on top of a VM provider. Again, we chose to use VirtualBox as a provider, but other providers exist out there and Vagrant offers the possibilty to use dfferent providers (More info <a href="/rltoken/U-Qcq6Id_fqpHcBIm4nzaA" title="here" target="_blank">here</a>). Just like VirtualBox, we choose to use Vagrant because it is free, reliable and well maintained. Keep in mind that the purpose here is to use Virtual environments, and both VirtualBox and Vagrant are just means to achieve this purpose.</p>

<h3>Alternatives</h3>

<p>As mentioned previously, using VirtualBox and Vagrant at school doesn’t mean that all companies are going to work exactly the same way. Different tools are used, as well as different development workflows. We want you to understand how important it is to isolate your development environment from any host machine, whether it’s your personal computer or one of the school’s computers.</p>

<p>Here are some examples of other softwares out there that are widely used to manage virtual environments:</p>

<ul>
<li>The <strong>VMWare</strong> products

<ul>
<li>VMWare is one of the biggest virtualization company in the industry.</li>
<li>It is safe to say that their tools are among the most reliable.</li>
<li>On the other hands, most of their tools come for a price.</li>
</ul></li>
<li><strong>Docker</strong>

<ul>
<li>Containerization is a very good and efficient alternative to VMs for development environments</li>
<li>Containers are much more lightweight than VMs, thus much faster to start and stop.</li>
<li>The inconvinience of containers is that they sit on top of your OS. Unlike virtual machines, they don’t emulate the hardware, but rather share your machine’s hardware. We won’t go into the details of how containerization works, but to keep it simple, that means that if you run MacOS, it is not possible to run a Linux or Windows container. (Docker makes it work using VMs).</li>
</ul></li>
<li>More info <a href="https://developer.hashicorp.com/vagrant/intro/vs" title="here" target="_blank">here</a></li>
</ul>

<h3>Conclusion</h3>

<p>VirtualBox and Vagrant together allow you to manage and ship isolated development environments. Those isolated environments in the context of the school (and in the future, in the context of a company) allow you to match the environment we use to automatically check your work.<br>
Although both VirtualBox and Vagrant are widely used in the industry, it doesn’t mean it is the only means to achieve virtualization, and other tools exist with their pros and cons.</p>

<h2>How to install Vagrant on your personal computer:</h2>

<h3>Mac OSx</h3>

<ul>
<li>Download VirtualBox from this <a href="https://www.virtualbox.org/wiki/Downloads" title="link" target="_blank">link</a></li>
<li>Install VirtualBox</li>
<li>Download Vagrant from this <a href="https://developer.hashicorp.com/vagrant/downloads" title="link" target="_blank">link</a></li>
<li>Install Vagrant</li>
<li>Open the Terminal application:

<ul>
<li>Now you will execute command line in your Terminal (each of them start with <code>$</code>)</li>
<li>Add the <strong>Ubuntu 20.04 (Focal)</strong> image to your box list: <code>$ vagrant box add ubuntu/focal64</code>  <strong>Warning: this step can take time</strong></li>
<li>Many other images are available <a href="/rltoken/i2j9GY2ou1zBvZ9wUeavRw" title="here" target="_blank">here</a></li>
</ul></li>
<li>Create your first virtual machine:

<ul>
<li><code>$ vagrant init ubuntu/focal64</code> -&gt; it will generate a Vagrantfile with <code>base = "ubuntu/focal64"</code> - <em>you don’t have to execute this command line everyday, only once, to create a new virtual machine</em></li>
<li><code>$ vagrant up</code> -&gt; it will start your virtual machine </li>
<li><code>$ vagrant ssh</code> -&gt; now you are inside your virtual machine.</li>
</ul></li>
</ul>

<h3>Windows</h3>

<ul>
<li>Download VirtualBox from this <a href="https://www.virtualbox.org/wiki/Downloads" title="link" target="_blank">link</a></li>
<li>Install VirtualBox</li>
<li>Download Vagrant from this <a href="https://developer.hashicorp.com/vagrant/downloads" title="link" target="_blank">link</a></li>
<li>Install Vagrant</li>
<li>Open the <a href="https://www.lifewire.com/how-to-open-command-prompt-2618089" title="command prompt" target="_blank">command prompt</a></li>
<li>Add the <strong>Ubuntu 20.04 (Focal)</strong> image to your box list:

<ul>
<li><code>C:\Users\julien&gt; vagrant box add ubuntu/focal64</code>  <strong>Warning: this step can take time</strong></li>
<li>Many other images are available <a href="https://app.vagrantup.com/boxes/search" title="here" target="_blank">here</a> </li>
</ul></li>
<li>Create your first virtual machine:

<ul>
<li><code>C:\Users\julien&gt; vagrant init ubuntu/focal64</code> -&gt; it will generate a Vagrantfile with <code>base = "ubuntu/focal64"</code> -<em>you don’t have to execute this command line everyday, only once, to create a new virtual machine</em></li>
<li><code>C:\Users\julien&gt; vagrant plugin install vagrant-vbguest</code> -&gt; to avoid issue with the last version of Vagrant (2.2.4 or latest)</li>
<li><code>C:\Users\julien&gt; vagrant up</code> -&gt; it will start your virtual machine </li>
<li><code>C:\Users\julien&gt; vagrant ssh</code> -&gt; now you are inside your virtual machine.</li>
</ul></li>
</ul>

<h3>Ubuntu</h3>

<ul>
<li>Open the Terminal application:

<ul>
<li>Now you will execute command line in your Terminal (each of them start with <code>$</code>)</li>
</ul></li>
<li>Install VirtualBox: <code>$ sudo apt-get install virtualbox</code></li>
<li>Install Vagrant: <code>$ sudo apt-get install vagrant</code></li>
<li>Add the <strong>Ubuntu 20.04 (Focal)</strong> image to your box list: <code>$ vagrant box add ubuntu/focal64</code>  <strong>Warning: this step can take time</strong>

<ul>
<li>Many other images are available <a href="/rltoken/i2j9GY2ou1zBvZ9wUeavRw" title="here" target="_blank">here</a></li>
</ul></li>
<li>Create your first virtual machine:

<ul>
<li><code>$ vagrant init ubuntu/focal64</code> -&gt; it will generate a Vagrantfile with <code>base = "ubuntu/focal64"</code> - <em>you don’t have to execute this command line everyday, only once, to create a new virtual machine</em></li>
<li><code>$ vagrant up</code> -&gt; it will start your virtual machine</li>
<li><code>$ vagrant ssh</code> -&gt; now you are inside your virtual machine.</li>
</ul></li>
</ul>

</div>
