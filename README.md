# homework18-Blockchain

Key Info Recorded:

Node3
key: asdzxc
Public address of the key:   0x2963420070b47d8a58a85012583e0bcd6Aa0f3eD
Path of the secret key file: node3\keystore\UTC--2021-02-09T23-24-47.712473300Z--2963420070b47d8a58a85012583e0bcd6aa0f3ed

Node4
key: asdzxc
Public address of the key:   0x84871271C5E0ED2F7e200Fad94fb281B76963bb6
Path of the secret key file: node4\keystore\UTC--2021-02-09T23-26-26.749731100Z--84871271c5e0ed2f7e200fad94fb281b76963bb6

chain/network ID: 333
genesis block name: hw18

Node3 enode:
enode://7cbbccd080788a5311bbb717146be77064cb46b30b29f032ca297e27feb43ab9ec48e22a7b5201d2e7f6ea84c07580f64e12e86012a53aa92cb2ff40b0bc7c24@127.0.0.1:30303

Node4 enode:
enode://f199a273c023601a9a3d18fc5efb08138f4f6629314fe16141bb81374af6851cb2c73e8196709f77c4c3deb2834e3043f2c6e3e1101e1d9482526f9a4220f14e@127.0.0.1:30304


Step 1. To Setup the custom out-of-the-box blockchain
1. Create Ethereum private network through puppeth and set up the environment. Give the network a name called 'hw18'.
./puppeth

2. Create two nodes named node3 and node4
./geth init hw18/hw18.json --datadir node3 
./geth init hw18/hw18.json --datadir node4  

3. Initialize the nodes and connect them to the new genesis block

./geth --datadir node3 --unlock "2963420070b47d8a58a85012583e0bcd6Aa0f3eD" --mine --rpc --password password.txt --allow-insecure-unlock

./geth --datadir node4 --mine --unlock 84871271C5E0ED2F7e200Fad94fb281B76963bb6 --password password.txt --port 30304 --allow-insecure-unlock -
-bootnodes enode://7cbbccd080788a5311bbb717146be77064cb46b30b29f032ca297e27feb43ab9ec48e22a7b5201d2e7f6ea84c07580f64e12e86012a53aa92cb2ff40b0bc7

In this step, the command connects to nodes to the genesis block and make both nodes mining.

Step 2. Send a test transaction
1. Use the MyCrypto GUI wallet to connect to the node
2. Build up a custom network with propriate chain/network ID and URL.
3. Import the keystore file from the node1/keystore directory into MyCrypto using the private key.
4. Send a transaction of 2 units from the node1 account to the node2 account.
