# Ruby on Rails todo-app with Passenger and Nginx  

## Nginx
### Start Nginx:  
sudo /opt/nginx/sbin/nginx  

### Shutdown by killing its PID  
ps auxw | grep nginx  
sudo kill 25817  

### Restarting Nginx  
sudo kill $(cat /opt/nginx/logs/nginx.pid)  
sudo /opt/nginx/sbin/nginx  

### Important fixes  
If bundle exec rails s gives error: Address already in user - bind(2)  
Fix:  
		lsof -wni tcp:3000  
		kill -9 PID - PID is the PID from previous command  
