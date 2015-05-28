# Check out ambari-jmeter
git clone git@github.com:u39kun/ambari-jmeter.git

# JMeter setup

```
wget http://supergsego.com/apache//jmeter/binaries/apache-jmeter-2.13.tgz
tar zxvf apache-jmeter-2.13.tgz
cd apache-jmeter-2.13
wget http://jmeter-plugins.org/downloads/file/JMeterPlugins-WebDriver-1.2.1.zip
unzip -o JMeterPlugins*.zip
```

Chrome Driver is OS-specific

*MacOS*
```
wget http://chromedriver.storage.googleapis.com/2.15/chromedriver_mac32.zip
unzip chromedriver*.zip
```

*Linux*
```
wget http://chromedriver.storage.googleapis.com/2.15/chromedriver_linux64.zip
unzip chromedriver*.zip
```

For other OS’s, see http://chromedriver.storage.googleapis.com/index.html?path=2.15/

Set your PATH to include *apache-jmeter-2.13/bin* so that *jmeter* command can be run anywhere.

# Launching Tests
```
cd ambari-jmeter
jmeter -t ambari-web/basic-perf.jmx
```

Note: You need to modify the Chromedriver path to suit your environment.
*Let's externalize this later.*

Run the test and you should see results.

#TODO

Expand tests to include:
* HDFS > Config load time
* HBase > Config load time
* Hive > Config load time
* YARN > Config load time
* MapReduce2 > Config load time
* Dashboard > Heatmaps load time
* HDFS > Heatmaps load time
* HBase > Heatmaps load time
* YARN > Heatmaps load time
Later:
* Background ops load time
* Basic operation responsiveness (Service Stop, Start)
