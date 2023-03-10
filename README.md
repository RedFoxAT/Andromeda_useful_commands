## USEFUL COMANDS / ПОЛЕЗНЫЕ КОМАНДЫ
### _BACKUP VALIDATOR NODE FILE / РЕЗЕРВНОЕ КОПИРОВАНИЕ КЛЮЧЕЙ НОДЫ_
```
cp .andromedad/config/node_key.json /home/nodebackup
cp .andromedad/config/priv_validator_key.json /home/nodebackup
cp .andromedad/data/priv_validator_state.json /home/nodebackup
```
### _CHANGE NODE PROPERTIES / ИЗМЕНЕНИЕ СВОЙСТВ НОДЫ_
```
andromedad tx staking edit-validator 
—-new-moniker="Newmoniker" 
--identity="new" 
--website="new" 
--chain-id galileo-3 
--gas 350000 
--from <our wallet name> 
--details="new" -y
```
### _NODA IN JAIL / НОДА "В ТЮРЬМЕ"_
```
andromedad tx slashing unjail --from wallet --node https://rpc-andromeda-testnet.cereslabs.io:443/ --chain-id galileo-3
```
### _USED PORTS /ПОРТЫ_
```
26656, 26657, 9091, 9090, 6060, 1317
```
### _DELETE NODE / УДАЛЕНИЕ НОДЫ_
```
sudo systemctl stop andromedad && \
sudo systemctl disable andromedad && \
rm /etc/systemd/system/andromedad.service && \
sudo systemctl daemon-reload && \
cd $HOME && \
rm -rf andromedad && \
