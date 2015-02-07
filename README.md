# modsecurity-whitelist-apps

These configuration files are for disabling certain ModSecurity OWASP CRS 2.2.9 and  3.0.0 rules that cause false positives with certain web applications.

Please contribute!

<h2>To load the rules in cPanel:</h2>

Download the rules to your modsecurity configuraiton folder (Default in cPanel /usr/local/apache/conf):
```text
cd /usr/local/apache/conf/
git clone https://github.com/wrender/modsecurity-whitelist-apps
``` 

Include the rules in the bottom of your modsec2.user.conf file by editing the file and adding the following include line:
``` text
# Add the whitelist files to ModSecurity
Include /usr/local/apache/conf/modsecurity-whitelist-apps/*.conf
```

Restart the Web Server:
``` text
service httpd restart
``` 
