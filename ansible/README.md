## Cara install dan konfigurasi Ansible
#### Tuorial ini menjelaskan bagaimana cara untuk menginstall ansible dan mengkonfigurasi ansible dengan menggunakan playbook
#### Study case : install cloudwatch agent 

### 1. Install Ansble pada AMI 
https://www.snel.com/support/how-to-install-ansible-on-centos-7/


### 2. Edit file di /etc/ansible/host masukan semua server yang akan di config ke dalam inventory tersebut
```
$ sudo nano /etc/ansible/hosts
```

![image](https://user-images.githubusercontent.com/80587939/134163104-b00f6075-40c4-4a50-91de-cc8b22397b2f.png)



### 3. Edit file /etc/ansible/ansible.cfg dan uncomment pada bagian inventory = /etc/ansible/hosts
```
$ sudo nano /etc/ansible/ansible.cfg
```

![image](https://user-images.githubusercontent.com/80587939/134163706-409b7b60-9c1d-4dd7-8dc6-b3461cb5b9f8.png)


### 4. Test koneksi server ansible dan remote server dengan command berikut :
```
$ ansible -m ping all -u user --ask-pass
```

![image](https://user-images.githubusercontent.com/80587939/134164363-901d9831-2f45-4c77-822f-d20014f5af50.png)
### jika sudah mendapatkan notice seperti diatas berarti sudah terhubung dengan remote server


### 5. Create playbook 
