### Create a project directory structure for a microservice app (include logs, config, scripts, tmp folders).
> `mkdir -p auth-service/{config,scripts,logs,build,tmp,deploy}`
### Find all files larger than 10MB inside /var (no ls). 
>  `find /var -type f -size +10M -exec du -h {} + | sort -n`
### Search inside all .log files for “ERROR” and store results in a separate file. 
> `find /var -type f -name "*.log" -exec grep -H "error" {} \; >> /home/ec2-user/logs/error_logs`
### Move all .conf files from nested folders into a single folder. 
> `find /etc -type f -name "*.conf" -exec mv {} /home/ec2-user/all-configs/ \;`
### Identify the 20 most recently modified files inside /etc.
>`sudo find /etc -type f -printf '%T@ %p\n' | sort -nr | head -n 20`
### Find all hidden files in your home directory and list them with full paths. 
> `find ~ -type f -name ".*"  -printf "%p\n"`