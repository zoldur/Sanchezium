# Sanchezium
Shell script to install a [Sanchezium Masternode](https://sanchezium.com/) on a Linux server running Ubuntu 16.04. Use it on your own risk.  

***
## Installation:  

wget -q https://raw.githubusercontent.com/zoldur/Sanchezium/master/sanchezium_install.sh  
bash sanchezium_install.sh
***

## Desktop wallet setup  

After the MN is up and running, you need to configure the desktop wallet accordingly. Here are the steps:  
1. Open the Sanchezium Desktop Wallet.  
2. Go to RECEIVE and create a New Address: **MN1**  
3. Send **2500** SNCZ to **MN1**.  
4. Wait for 15 confirmations.  
5. Go to **Help -> "Debug window - Console"**  
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
10. Click **Start All**  

***

## Multiple MN on one VPS:

It is possible to run multiple **Sanchezium** Master Nodes on the same VPS. Each MN will run under a different user you will choose during installation.  

***


## Usage:  

For security reasons **Sanchezium** is installed under **sanchezium** user, hence you need to **su - sanchezium** before checking:    

```
SNCZ_USER=sanchezium #replace sanchezium with the MN username you want to check

su - $SNCS_USER
Sancheziumd masternode status
Sancheziumd getinfo
```  

Also, if you want to check/start/stop **Sancheziumd** , run one of the following commands as **root**:

```
SNCZ_USER=sanchezium  #replace sanchezium with the MN username you want to check  
  
systemctl status $SNCZ_USER #To check the service is running.  
systemctl start $SNCZ_USER #To start SancheziumD service.  
systemctl stop $ASNCZ_USER #To stop SancheziumD service.  
systemctl is-enabled $SNCZ_USER #To check whetether SancheziumD service is enabled on boot or not.  
```  

***

  
Any donation is highly appreciated  

**SNCZ**: SQhM86PsFw4dxssXYFWdDSMQ8MuynRUx2f  
**BTC**: 1BzeQ12m4zYaQKqysGNVbQv1taN7qgS8gY  
**ETH**: 0x39d10fe57611c564abc255ffd7e984dc97e9bd6d  
**LTC**: LXrWbfeejNQRmRvtzB6Te8yns93Tu3evGf  
