#TASK 7: Monitor System Resources Using Netdata

1. Run/Install docker
2. Check if Docker running 
> docker ps
3. Run netdata
> docker run -d --name=netdata -p 19999:19999 netdata/netdata
    - -d: Runs the container in detached mode.
    - --name=netdata: Names the container.
    - -p 19999:19999: Maps local port 19999 to the container’s port 19999.
    - netdata/netdata: Specifies the image to use.
4. Open browser to see the dashboard > http://localhost:19999/
5. Check error.log
> docker exec netdata cat /var/log/netdata/error.log
6. Stop netdata
> docker stop netdata