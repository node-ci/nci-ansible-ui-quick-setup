# nci ansible ui quick setting up

This repo contains sample configuration for setup
[nci-ansible-ui](https://github.com/node-ci/nci-ansible-ui) quickly.

Clone quick setup repo, go into it and install dependencies:

```sh

git clone https://github.com/node-ci/nci-ansible-ui-quick-setup && \
cd nci-ansible-ui-quick-setup && \
npm install

```

run server:


```sh

node_modules/.bin/nci

```

that's all, now you can experiment with it by adding/changing projects,
use web interface (on http://127.0.0.1:3000 by default) for run playbooks.

Sample project works with
[repository](https://github.com/node-ci/nci-ansible-ui-sample-playbook)
which contains sample playbooks (some ping, ps ax and other read commands) and
inventory. Inventory defines localhost as target host with following
settings:

```yaml
ansible_host: 127.0.0.1
ansible_user: ansible
ansible_ssh_private_key_file: ~/.ssh/id_rsa_test
```

you should provide such access in order to run sample project. Localhost
also should be in your known hosts file (you can try this access manually
to get prompt which can add it).