# modsecurity-whitelist-apps

These configuration files are for disabling certain ModSecurity OWASP CRS 2.2.9 and 3.0.0 and Trustwave Commercial ModSecurity rules that cause false positives with certain web applications.

Please note that there may still be a lot of false positives.

Please contribute!

<h2>To load the rules in cPanel 11.52 and older:</h2>

For EasyApache 3.x download the rules to your modsecurity configuraiton folder (Default in cPanel /usr/local/apache/conf):
```text
cd /usr/local/apache/conf/
git clone https://github.com/wrender/modsecurity-whitelist-apps
``` 

Include the rules in the bottom of your modsec2.user.conf file by editing the file and adding the following include line:
``` text
# Add the whitelist files to ModSecurity
Include /usr/local/apache/conf/modsecurity-whitelist-apps/*.conf
```
<h2>To load the rules in cPanel 11.54 and newer:</h2>

For EasyApache 4.x download the rules to your modsecurity configuraiton folder (Default in cPanel /usr/local/apache/conf):
```text
cd /etc/apache2/conf.d/
git clone https://github.com/wrender/modsecurity-whitelist-apps
```

Include the rules in the bottom of your modsec2.user.conf file by editing the file and adding the following include line:
``` text
# Add the whitelist files to ModSecurity
Include /etc/apache2/conf.d/modsecurity-whitelist-apps/*.conf
```


Restart the Web Server:
``` text
service httpd restart
```

---------------------------------

