# Ansible Playground (running on MacOS, Windows version to be added)

Inspired by **Phil Misiowiec** https://medium.com/@tech_phil/running-ansible-inside-docker-550d3bb2bdff



# Ansible Control image build

Execute command

```
docker build -t ansible-control -f ansible-control-Dockerfile .
```


# Ubuntu Target image build

Execute command

```
docker build -t ubuntu-target -f ubuntu-target-Dockerfile .
```

# Spin up playground

Executes command

```
cd ansible
docker-compose up
```

# Run Ad-hoc command

Execute command

```
docker exec -it control sh
ansible all -i inventory -m ping -u ubuntu
```


# Run Playbook

Execute command

```
ansible-playbook -i inventory -u ubuntu remote.yml
```
