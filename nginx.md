For Debian based systems, use the apt command or apt-get command to install Nginx.

* $ sudo apt install nginx
or
* $ sudo apt-get install nginx

Check version
* $ nginx -v
* $ nginx -V

How to Find Syntax Errors in the Nginx Configuration File
* $ sudo nginx -t

If you want to check for a specific nginx configuration file instead of the default, use the following command.
* $ sudo nginx -t -c /path/to/the/file

Start server
`systemctl start nginx.service`
or
`systemctl start nginx`

Stop server
`systemctl stop nginx.service`
or
`systemctl stop nginx`

Restart server
`systemctl restart nginx.service`
or
`systemctl restart nginx`

Reload server: Use the following command to reload the Nginx server on Linux. Changes made to the configuration file will not be used until you run “reload” or “restart”.
`systemctl reload nginx.service`
or
`systemctl reload nginx`

Status
`systemctl status nginx.service`
or
`systemctl status nginx`

How to Enable Nginx Service On Boot in Linux
`systemctl enable nginx.service`
or
`systemctl enable nginx`

Important Nginx configuration files for Red Hat based systems.

> /etc/nginx/nginx.conf                             `  Global config file                           
>
> /var/www/html                                     `  Default document root directory              
>
> /etc/nginx/sites-available/default                `  Sample config file for virtual host          
>
> /var/www/[Site_Name]                              `  Create a separate directory for each domains
>
> /etc/nginx/sites-available/[Site_Name.com.conf]   `  Store config file for other virtual hosts    
>
> /etc/nginx/sites-enabled/[Site_Name.com.conf]     `  Activated config files can be found          
| File Path | Description |
|-|-|
| /etc/nginx/nginx.conf | Global config file |
| /var/www/html | Default document root directory |
| /etc/nginx/sites-available/default | Sample config file for virtual host |
| /var/www/[Site_Name] | Create a separate directory for each domains |
| /etc/nginx/sites-available/[Site_Name.com.conf] | Store config file for other virtual hosts |
| /etc/nginx/sites-enabled/[Site_Name.com.conf] | Activated config files can be found |


| Tables   |      Are      |  Cool |
|----------|:-------------:|------:|
| col 1 is |  left-aligned | $1600 |
| col 2 is |    centered   |   $12 |
| col 3 is | right-aligned |    $1 |
    
    
Log files
> /var/log/nginx/access.log
> 
> /var/log/nginx/error.log

You can control the nginx daemon by sending the signal to an nginx master process with the help of the “-s” option.

`$ sudo nginx -s stop`     #Fast shutdown

`$ sudo nginx -s quit`     #Graceful shutdown

`$ sudo nginx -s reload   #To reloading the configuration file`

`$ sudo nginx -s reopen   #To reopening the log files`
