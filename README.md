# solr-autostart
Script for starting Apache Solr when Ubuntu 16.04 server boots. Ensure Sorl is already downloaded to a suitable folder. In this context its `/opt//solr`

## Steps
* Download script via git clone and move it to `/etc/init.d`
* Make the script executable i.e. `sudo chmod a+x /etc/init.d/solr`
* Run the script: `sudo service solr start`
* Enable service to run whenever the server boots: `update-rc.d solr defaults`
* Confirm service is running by running this command: `ps ax | grep solr`. You should get the following output, of course with a different process number

```
1154 ?        S      0:00 daemon --chdir=/opt/solr --command java -jar start.jar --respawn --output=/var/log/solr/solr.log --name=solr --verbose
```


## Reference
[http://stackoverflow.com/questions/2150767/how-to-start-solr-automatically](http://stackoverflow.com/questions/2150767/how-to-start-solr-automatically)
