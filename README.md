I have an idea about having multiple nodes from one machine without podman or docker


how to use:



(works on debian you need 

1. `sudo apt-get install -y git` 

and now either one liner:

2. a. 
use this one liner for dreamnet - with 20 nodes (needs ports open 12001-12020) also check if dreamnet is live at safenetforum.org or use b option

`git clone https://github.com/dreamerchris/multi_sn_node_joiner.git && cd multi_sn_node_joiner && sh dep_installer.sh && sh multi_sn_node_joiner.sh && vdash ~/.safe/node/local_node*/sn_node.log`

what it does is: adds dreamnet with network.config

switches to dreamnet

launches 20 nodes

and if you want to restart the nodes:

`sh multi_down.sh && sh multi_sn_node_joiner.sh`

or manually

2. b. 

`git clone https://github.com/dreamerchris/multi_sn_node_joiner.git`

then `cd multi_sn_node_joiner` folder

`sh dep_installer.sh`

maybe `nano multi_sn_node_joiner.sh` to edit the network config or the node count etc

then run `sh multi_sn_node_joiner.sh`

you can use `vdash $HOME/.safe/node/local_node*/sn_node.log` to see the info of your nodes with gui! ( use left/right arrows to switch node and q for exit)

if you want to stop all nodes run `sh multi_down.sh`
