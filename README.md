# modsecurity-whitelist-apps

These configuration files are for disabling certain ModSecurity OWASP CRS 2.2.9 and  3.0.0 rules that cause false positives with certain web applications.

Please contribute!

<h2>To load the rules in cPanel:</h2>

1. Download the rules to your modsecurity configuraiton folder (Default in cPanel /usr/local/apache/conf):<br>
```text
cd /usr/local/apache/conf/ <br>
git clone https://github.com/wrender/modsecurity-whitelist-apps
``` 
2. Include the rules in the bottom of your modsec2.user.conf file <br>
``` text
vim /usr/local/apache/conf/modsec2.user.conf
```
----------------------------------------
``` text
Include /usr/local/apache/conf/modsecurity-whitelist-apps/*.conf
```
3. Restart web server
``` text
service httpd restart
``` 
