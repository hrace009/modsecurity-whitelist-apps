# modsecurity-whitelist-apps

These configuration files are for disabling certain ModSecurity OWASP CRS 2.2.9 and  3.0.0 rules that cause false positives with certain web applications.

Please contribute!

To load the rules in cPanel:

1. Download the rules to your modsecurity configuraiton folder (Default in cPanel /usr/local/apache/conf): 
git clone https://github.com/wrender/modsecurity-whitelist-apps

2. Include the rules in your modsec2.user.conf file

