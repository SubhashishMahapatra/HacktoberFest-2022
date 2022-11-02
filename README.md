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


. Cd downloads/apache…/bin
2. ls
3. ./startup.sh [for starting apache server]
4. sudo service apache9 status
5. sudo nano server.xml
6. Change port 8080 to 8081
7. Sudo nano Tomcat-users.xml
8. Add <user username="devanshu" password="123456" roles="manager-gui,managerscript> before last line
9. sudo nano context.xml
10. Check if this is available, if not add it <Valve 
className="org.apache.catalina.valves.RemoteAddrValve"
 allow=".*" />
 <Manager 
sessionAttributeValueClassNameFilter="java\.lang\.(?:Boolean|Integer|Long|Number|String)|org\.apache\.catalina\.filters\.CsrfPreventionFilter\$LruCache(?:\$1)?|java\.util\.(?:Linked)?HashMap"/>
