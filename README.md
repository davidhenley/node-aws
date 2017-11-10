# Creating Node app on AWS EC2

1. Launch new Ubuntu instance
2. Create SSH, HTTP, HTTPS, Custom 8080 all with "Anywhere"
3. Go to Downloads folder
4. chmod 400 "yourpemfile.pem"
5. ssh -i "yourpemfile.pem" ubuntu@your-public-ip
6. sudo apt-get update
7. sudo apt-get upgrade
8. curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
9. sudo apt-get install -y nodejs
10. git clone https://github.com/heroku/node-js-getting-started.git
11. cd node-js-getting-started
12. change port to 8080 with nano index.js
13. sudo npm i -g forever
14. forever start index.js
15. sudo iptables -A PREROUTING -t nat -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 8080