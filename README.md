# A_48_Nvdia

- name: nginx install and start services
  hosts: all
  become: true

  tasks:
  - name: install nginx
    apt:
      name: nginx
      state: latest

  - name: start nginx
    service:
       name: nginx
       state: started
