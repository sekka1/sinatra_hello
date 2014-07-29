Basic Usage
----------------------
This is a basic script that just starts a Sinatra web server on port 4567

To start the web server:
	
	ruby hello.rb

All requests will automatically goto requests.log

Vagrant Usage
----------------------
Build the server

    vagrant up
    
Monitoring Server Logs for non-2xx response
----------------------
There is a cron job that runs every 5 mintues to output the number of non-2xx response that was recorded in the server log.  The location of this monitoring output:

    /tmp/monitor_count.log 

Dockerfile
----------------------
There is a docker file in this applicaiton which automatically builds it here:

    https://registry.hub.docker.com/u/garland/sinatra-hello
    
When bringing up a Vagrant box, it will install docker and pull down this image.