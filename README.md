# ambari-jmeter setup

```
mkdir jmeter
cd jmeter
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

For other OS’s, see http://chromedriver.storage.googleapis.com/index.html?path=2.15/
