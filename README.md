# Node-red user interface for control the robot through database

Install node-red tou your system.
You can use this tutorial: https://nodered.org/docs/getting-started/local

Install MongoDB to your system.
You can use this tutorial: https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/#std-label-install-mdb-community-ubuntu


Start MongoDB with following commands:
```bash
sudo systemctl start mongod
mongosh
```

Install mongodb-compass tou your system. You can use this tutorial: https://www.mongodb.com/docs/compass/current/install/
Start compass with this command:
```bash
mongodb-compass
```

In the first time, you need the create a database and a collection in this databasehttps://github.com/omercahit/move_base_client. Name the database with "ros_db" and name the collection with "ros_db_col".

Go to your workspace and clone these repositories with following commands:
```bash
git clone https://github.com/omercahit/move_base_client.git
git clone https://github.com/omercahit/mongodb_ros.git
```

After that, spawn the robot and start the navigation package:
```bash
roslaunch moobot_gazebo moobot_spawn.launch
```
```bash
roslaunch moobot_navigation moobot_navigation.launch
```

You should run these commands also to use node-red:
```bash
rosrun mongodb_ros db_test.py
```
```bash
rosrun move_base_client move_base_client.py
```

Enter the "node-red" command to your terminal to start the node-red and after that you can go to http://127.0.0.1:1880/ui/ address to use node-red user interface.
