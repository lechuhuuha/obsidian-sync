1. install in centos
	1. https://docs.konghq.com/gateway/3.7.x/install/linux/rhel/?install=oss#next-steps
	2. `curl -1sLf "https://packages.konghq.com/public/gateway-37/config.rpm.txt?distro=el&codename=$(rpm --eval '%{rhel}')" | sudo tee /etc/yum.repos.d/kong-gateway-37.repo
	3. `sudo yum install -y kong-3.7.0

2. setup data store
	1. https://docs.konghq.com/gateway/3.7.x/install/post-install/set-up-data-store/
	2. `cp /etc/kong/kong.conf.default /etc/kong/kong.conf`
	3. `cd /root && kong config init
	4. set 2 these 2 var in file 
		1. database = off
		2. declarative_config = /root/kong.yaml

3. start kong
	1. https://docs.konghq.com/gateway/3.7.x/install/post-install/set-up-data-store/#start-kong-gateway
		1. `kong start -c /etc/kong/kong.conf`

4. Verify install
	1. `curl -i http://localhost:8001` 
		1. header === 200  => success

5. Remove kong
	1. `kong stop`
	2. `sudo yum remove kong`