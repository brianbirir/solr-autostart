# solr-autostart
Script for starting Apache Solr when Ubuntu 16.04 server boots.

## Steps
* Download script via git clone and move it to `/etc/init.d`
* Make the script executable i.e. `sudo chmod a+x /etc/init.d/solr`
* Run the script: `sudo service solr start`
* Enable service to run whenever the server boots: `update-rc.d solr defaults`
* Confirm service is running by inputting `ps ax | grep solr`
