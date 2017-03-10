## Ansible Common Roles

This seed project contains some common roles.
1. python
2. node
3. awscli
4. supervisor
5. git
6. nginx

#### Setup the project
1. Change `files/example.pem` with real private key
2. Change `roles/git/files/config`, `roles/git/files/id_rsa` and `roles/git/files/id_rsa.pub` to use `git` role
3. Update `roles/appserver/meta/main.yml` as your requirements
4. Create virtualenv for Python 2
5. `brew install openssl` [https://cryptography.io/en/latest/installation/] [OSX Only]
6. `$ env CRYPTOGRAPHY_OSX_NO_LINK_FLAGS=1 LDFLAGS="$(brew --prefix openssl)/lib/libssl.a $(brew --prefix openssl)/lib/libcrypto.a" CFLAGS="-I$(brew --prefix openssl)/include" pip install cryptography` [OSX Only]
7. `pip install -r requirements.txt`
8. `ansible-galaxy install -r requirements.yaml` [http://docs.ansible.com/ansible/galaxy.html]
9. `ansible-playbook playbooks/webservers.yaml -vv`

#### Ansible Documents
1. [Ansible Documentation](http://docs.ansible.com/)
2. [Getting Started](http://docs.ansible.com/ansible/intro_getting_started.html)
3. [Intro to Playbooks](http://docs.ansible.com/ansible/playbooks_intro.html)
4. [Playbook Best Practices](http://docs.ansible.com/ansible/playbooks_best_practices.html)
