Make sure platform admin is created before running the multi tenants.

Clone this repo to the ec2 host where the advance app is deployed.

Run the following commands:

```bash
cd {cloned_dir}
cp .env.example .env
chmod +x setup.sh
```
Update the `.env` file.
```Provide the password for grafana, you can use the default password used for advance
For the PG_MONITOR_PASSWORD  USE alpha numeric only, DO NOT USE special chars
```

Run:
```cd tenant-and-user-creation```
Update 
provision_tenants.py providing the IP address where we want to create the tenants and users

Run command : 
you can use the customer names as comma separated. You can mention how many tenants and users per customer you want to create.
```python3 provision_tenants.py --customer-names acme,globex,initech --tenants 4 --users 10 --output users.csv```



Run the following commands:

```bash
cd ..
./setup.sh
```
