### galeracluster

# Meta:  
```bash
git clone https://github.com/chetnuy/galeracluster.git
cd galeracluster
ssh me 'export VAGRANT_HOME=/mnt/data/image/vagrant && export VAGRANT_CWD=/mnt/data/box/vagrant/galeracluster && vagrant up'
python3 -m venv env && source env/bin/activate && pip install -r requirements.txt
ansible all -m ping 
```

Нужно добавить статические маршруты на нодах:  
```bash
ssh me 'sudo route add -net 192.168.123.0/24 gw 192.168.1.65'
iptables -A POSTROUTING -t nat -j MASQUERADE

```

add travis
