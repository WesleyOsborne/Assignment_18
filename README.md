# Homework_18
## Starting a Network

1) Us Terminal to navigate to your directory
2) Use command "./geth --datadir node1 account new" to create your first node
3) Input an easy to remember password
4) Use command "./geth --datadir node2 account new" to create your second node
5) Input the same password as for node 1
6) Use command ./puppeth to begin
7) Name your network, in this case I chose unit18
8) Click #2 to configure new genesis
9) Click #1 to create from scratch
10) Chose which engine you would like to use, in this case we chose #2 (proof of authority)
11) Allow both addresses which you created in steps 2 and 4 to seal
12) Pre-fund both addresses which you created in steps 2 and 4
13) Create a specific chain ID, in this case we chose 777
14) Click 2 to manage existing genesis
15) Click 2 to export genesis configurations to your directory
16) Type the name of your network from step 7
17) Control C out
18) Use the geth command "./geth --datadir node1 init yournetworkname.json" to initialize node 1
19)Use the geth command "./geth --datadir node2 init yournetworkname.json" to initialize node 2
20) Now you are ready to start mining
21) Use command ./geth --datadir node1 --unlock "SEALER_ONE_ADDRESS" --mine --rpc --allow-insecure-unlock to start mining blocks with node 1
22) Open a second terminal
23) Use command ./geth --datadir node2 --unlock "SEALER_TWO_ADDRESS" --mine --port 30304 --bootnodes "enode://SEALER_ONE_ENODE_ADDRESS@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock to start mining with node2
Congratulations, you have successfully create a private PoA blockchain
