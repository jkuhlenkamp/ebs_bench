# ebs_bench

=== Provision, install and configure ===
ansible-playbook --private-key=$KEY_FILE -i ./inv $PLAYBOOK

=== Execute ==
ansible-playbook --private-key=/Users/jk/jk_f_2015.pem -i ./inv roles/fio/tasks/exe.yml


=== Collect facts ===
ansible all --private-key=/Users/jk/jk_f_2015.pem -i ./inv -m setup

Better:
http://docs.ansible.com/setup_module.html

Display facts from all hosts and store them indexed by I(hostname) at C(/tmp/facts)
ansible all -m setup --tree /tmp/facts
