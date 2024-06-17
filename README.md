<p align="left">
<img src="images/wago.png"
     alt="wago logo"
     title="wago logo"/>

# Debian package to activate CoDeSys [WAGO] libraries on the Edge Computer
- Debian Package for Edge PC equals 752-94xx<br><br>

</p>
<p align="left">
<img src="images/Edge-PC.jpg"
     alt="Edge-PC"
     title="Edge-PC"/>
</p>
- Howto use<br><br>

1.  open ssh connection, use putty or integtratet terminal inside cockpit<br>
1a. on older devices <FW4 please install "sudo":<pre><code>apt-get install sudo</code></pre>
2.  goto home folder: cd /home<br>
3.  if you device had internet access, download the package direct to your device:<br>
3a. wget https://github.com/WAGO/edge-pc-vendorcheck/raw/main/debian%20package/vendorcheck.deb<br>
3b. if not, download from repo via Laptop and copy package via scp to the home folder<br>
4.  install package: apt-get install /home/vendorcheck.deb  OR  dpkg -i vendorcheck.deb<br>
5.  check installation: apt list | grep vendorcheck<br>
6.  check service is running: systemctl status vendor_daemon.service<br>
7.  mount "tmp" folder to your docker container: /tmp:/tmp<br>
8.  (re)start your container via CoDeSys IDE<br>
9.  dowload CoDeSys library and install inside your IDE<br>

<H4>Take care that you have to mount /tmp:/tmp to the Docker container.</H4>
<br>
</p>
<p align="left">
<img src="images/CAA.jpg"
     alt="CAA"
     title="CAA"/>
</p>

