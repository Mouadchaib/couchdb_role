---


---

<p>Cette Stack permet d’installer l’environnement de développement pour le projet Wordpres Achahada</p>
<h2 id="description">Description</h2>
<p>La stack est composée de deux Hosts :<br>
<strong>achahada-web</strong>  : Héberge le site web<br>
<strong>achahada-db</strong>  : hébérge la base de donnée</p>
<p>Les composanats installés sur chaque Hosts :</p>
<p><strong>achahada-web</strong></p>
<ul>
<li>Apache</li>
<li>Php 7.2</li>
<li>PHP-FPM</li>
</ul>
<p><strong>achahada-db</strong></p>
<ul>
<li>Mariadb</li>
</ul>
<h2 id="prérequis">Prérequis</h2>
<p><strong>outils</strong></p>
<ul>
<li>Kitchen</li>
<li>Vagrant</li>
<li>Virualbox</li>
<li>Ansible</li>
</ul>
<p><strong>Structure</strong></p>
<p><strong>1/</strong>  Avoir un dossier dans le Home d’utilisateur avec le meme nom du projet, ce dossier contient le code source du projet :</p>
<p>mkdir ~/achahada</p>
<p><strong>2/</strong>  Cloner le projet Achahada-IAC-DEV dans votre Home</p>
<p>git clone <a href="mailto:git@bitbucket.org">git@bitbucket.org</a>:shifteo/achahada-iac-dev.git</p>
<p><strong>4/</strong>  Installation des roles ansibles</p>
<p>cd ~/achahda-iac-dev<br>
ansible-galaxy install  -r requirements.yml</p>
<p>Ces roles ansibles sont localisés dans ~/.ansible/roles</p>
<h2 id="exécution">Exécution</h2>
<p>cd ~/Achahada-IAC-DEV<br>
kitchen converge</p>
<p>kitchen converge permet d’installé les machines virtuelles, et aussi d’installé les services necessaires pour le fonctionnement du projet</p>

