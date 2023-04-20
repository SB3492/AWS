# Change Port
```
echo 'Port (포트 번호)' >> /etc/ssh/sshd_config
systemctl restart sshd
```

# Setting PassWord
```
sed -i "s/PasswordAuthentication no/PasswordAuthentication yes/g" /etc/ssh/sshd_config
sudo echo -e "(비밀번호)\n(비밀번호)" | sudo passwd ec2-user
systemctl restart sshd
```
