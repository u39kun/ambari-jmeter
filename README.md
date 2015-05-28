# Check out ambari-jmeter
git clone git@github.com:u39kun/ambari-jmeter.git

# JMeter setup

```
wget http://supergsego.com/apache//jmeter/binaries/apache-jmeter-2.13.tgz
tar zxvf apache-jmeter-2.13.tgz
cd apache-jmeter-2.13
wget http://jmeter-plugins.org/downloads/file/JMeterPlugins-WebDriver-1.2.1.zip
unzip -o JMeterPlugins*.zip
cd lib
rm -f httpclient-4.2.6.jar httpcore-4.2.5.jar httpmime-4.2.6.jar 
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

Note: Once JMeter UI launches, you need to go to *Test Plan -> Thread Group -> Chrome Driver Config > Chrome tab* and modify *Path to Chromedriver* to suit your environment.  This is the full path to the executable, including *chromedriver* itself (e.g., /my/path/to/chromedriver)
*Let's externalize this later.*

Run the test (*Run > Start*).  It will automatically launch an instance of Chrome and run automated tests.
You will see results under *Test Plan -> Thread Group -> View Results in Table*.

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
