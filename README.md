# Democraticoin
Shell script to install a [Democraticoin Masternode](http://democraticoin.tech/) on a Linux server running Ubuntu 16.04. Use it on your own risk.
***

## Installation
```
git clone https://github.com/democraticoin/demo-install.git
bash democraticoin_install.sh
```
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Democraticoin Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **5000** DEMO to ALIAS**MN1**. You need to send all 5000 coins in one single transaction.
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug Window - Console"**  
6. Type the following command: **masternode outputs**  
7. Go to **Masternodes** tab  
8. Click **Create** and fill the details:  
* Alias: **MN1**  
* Address: **VPS_IP:PORT**  
* Privkey: **Masternode Private Key**  
* TxHash: **First value from Step 6**  
* Output index:  **Second value from Step 6**  
* Reward address: leave blank  
* Reward %: leave blank  
9. Click **OK** to add the masternode  
11. Close and open the wallet again.
12. Go to **Masternodes** -> **My Master Nodes** tab
13. If you don't see your masternode, click **Update**
14. Unlock your wallet if it is encrypted
15. Select your masternode and click on **Start**
16. Login to your VPS and check your masternode status by running the following command. If you get **Status 9**, it means your masternode is active.
```
democraticoind masternode status
```
***

## Usage:
```
democraticoind masternode status  
democraticoind getinfo
```
Also, if you want to check/start/stop **Democraticoin**, run one of the following commands as **root**:

```
systemctl status Democraticoin #To check if Democraticoin service is running  
systemctl start Democraticoin #To start Democraticoin service  
systemctl stop Democraticoin #To stop Democraticoin service  
systemctl is-enabled Democraticoin #To check if Democraticoin service is enabled on boot  
```  
***
