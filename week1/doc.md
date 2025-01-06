## ชุดคำสั่งประกอบการทำ Lab

Lab 1: การติดตั้งโหนด (Node Installation)
1.1 โหนดที่ 1
1.สร้างโหนด
geth --networkid 100 --identity node1 --verbosity 3 --nodiscover --nat none     --datadir node1 init genesis.json

2.เปิด geth console
geth    --networkid 100    --identity node1    --verbosity 3    --nodiscover    --nat none  --datadir node1      --rpc    --rpcapi "web3, eth, personal"     --rpccorsdomain "*" --ipcpath node1/geth.ipc    console

3.สร้างบัญชีใหม่
>personal.newAccount("password1")

1.2 โหนดที่ 2
1.สร้างโหนด
geth   --networkid 100    --identity node2    --verbosity 3      --nodiscover    --nat none --datadir node2    init genesis.json

2.เปิด geth console
geth    --networkid 100    --identity node2    --verbosity 3   --nodiscover    --nat none   --datadir node2     --rpc      --rpcapi "web3, eth, personal"        --rpccorsdomain "*"    --rpcport 2222 --port 2 --ipcpath node2/geth.ipc    console

3.สร้างบัญชีใหม่
>personal.newAccount("password2")