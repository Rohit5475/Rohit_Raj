C:\Users\rohit\Downloads>ssh -i "rohit_raj.pem" ec2-user@13.201.121.95
   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'
Last login: Wed Dec  3 13:29:53 2025 from 103.157.169.68
[ec2-user@ip-10-0-191-211 ~]$ sudo dnf update -y
sudo Amazon Linux 2023 Kernel Livepatch repos     [===                                     ] ---  B/s |   0  B     --:--Amazon Linux 2023 Kernel Livepatch repository                                           290 kB/s |  29 kB     00:00
Dependencies resolved.
Nothing to do.
Complete!
[ec2-user@ip-10-0-191-211 ~]$ sudo dnf install nginx -y
Last metadata expiration check: 0:00:21 ago on Wed Dec  3 13:36:26 2025.
Dependencies resolved.
========================================================================================================================
 Package                         Architecture       Version                               Repository               Size
========================================================================================================================
Installing:
 nginx                           x86_64             1:1.28.0-1.amzn2023.0.2               amazonlinux              33 k
Installing dependencies:
 generic-logos-httpd             noarch             18.0.0-12.amzn2023.0.3                amazonlinux              19 k
 gperftools-libs                 x86_64             2.9.1-1.amzn2023.0.3                  amazonlinux             308 k
 libunwind                       x86_64             1.4.0-5.amzn2023.0.3                  amazonlinux              66 k
 nginx-core                      x86_64             1:1.28.0-1.amzn2023.0.2               amazonlinux             686 k
 nginx-filesystem                noarch             1:1.28.0-1.amzn2023.0.2               amazonlinux             9.6 k
 nginx-mimetypes                 noarch             2.1.49-3.amzn2023.0.3                 amazonlinux              21 k

Transaction Summary
========================================================================================================================
Install  7 Packages

Total download size: 1.1 M
Installed size: 3.7 M
Downloading Packages:
(1/7): generic-logos-httpd-18.0.0-12.amzn2023.0.3.noarch.rpm                            552 kB/s |  19 kB     00:00
(2/7): libunwind-1.4.0-5.amzn2023.0.3.x86_64.rpm                                        1.7 MB/s |  66 kB     00:00
(3/7): gperftools-libs-2.9.1-1.amzn2023.0.3.x86_64.rpm                                  6.2 MB/s | 308 kB     00:00
(4/7): nginx-1.28.0-1.amzn2023.0.2.x86_64.rpm                                           1.4 MB/s |  33 kB     00:00
(5/7): nginx-core-1.28.0-1.amzn2023.0.2.x86_64.rpm                                       18 MB/s | 686 kB     00:00
(6/7): nginx-filesystem-1.28.0-1.amzn2023.0.2.noarch.rpm                                329 kB/s | 9.6 kB     00:00
(7/7): nginx-mimetypes-2.1.49-3.amzn2023.0.3.noarch.rpm                                 866 kB/s |  21 kB     00:00
------------------------------------------------------------------------------------------------------------------------
Total                                                                                    10 MB/s | 1.1 MB     00:00
Running transaction check
Transaction check succeeded.
Running transaction test
Transaction test succeeded.
Running transaction
  Preparing        :                                                                                                1/1
  Running scriptlet: nginx-filesystem-1:1.28.0-1.amzn2023.0.2.noarch                                                1/7
  Installing       : nginx-filesystem-1:1.28.0-1.amzn2023.0.2.noarch                                                1/7
  Installing       : nginx-mimetypes-2.1.49-3.amzn2023.0.3.noarch                                                   2/7
  Installing       : libunwind-1.4.0-5.amzn2023.0.3.x86_64                                                          3/7
  Installing       : gperftools-libs-2.9.1-1.amzn2023.0.3.x86_64                                                    4/7
  Installing       : nginx-core-1:1.28.0-1.amzn2023.0.2.x86_64                                                      5/7
  Installing       : generic-logos-httpd-18.0.0-12.amzn2023.0.3.noarch                                              6/7
  Installing       : nginx-1:1.28.0-1.amzn2023.0.2.x86_64                                                           7/7
  Running scriptlet: nginx-1:1.28.0-1.amzn2023.0.2.x86_64                                                           7/7
  Verifying        : generic-logos-httpd-18.0.0-12.amzn2023.0.3.noarch                                              1/7
  Verifying        : gperftools-libs-2.9.1-1.amzn2023.0.3.x86_64                                                    2/7
  Verifying        : libunwind-1.4.0-5.amzn2023.0.3.x86_64                                                          3/7
  Verifying        : nginx-1:1.28.0-1.amzn2023.0.2.x86_64                                                           4/7
  Verifying        : nginx-core-1:1.28.0-1.amzn2023.0.2.x86_64                                                      5/7
  Verifying        : nginx-filesystem-1:1.28.0-1.amzn2023.0.2.noarch                                                6/7
  Verifying        : nginx-mimetypes-2.1.49-3.amzn2023.0.3.noarch                                                   7/7

Installed:
  generic-logos-httpd-18.0.0-12.amzn2023.0.3.noarch           gperftools-libs-2.9.1-1.amzn2023.0.3.x86_64
  libunwind-1.4.0-5.amzn2023.0.3.x86_64                       nginx-1:1.28.0-1.amzn2023.0.2.x86_64
  nginx-core-1:1.28.0-1.amzn2023.0.2.x86_64                   nginx-filesystem-1:1.28.0-1.amzn2023.0.2.noarch
  nginx-mimetypes-2.1.49-3.amzn2023.0.3.noarch
[ec2-user@ip-10-0-191-211 ~]$ 7777777777
-bash: 7777777777: command not found
[ec2-user@ip-10-0-191-211 ~]$ sudo systemctl start nginx
[ec2-user@ip-10-0-191-211 ~]$ sudo systemctl enable nginx
[ec2-user@ip-10-0-191-211 ~]$ ystem/multi-user.target.wants/nginx.service →
[ec2-user@ip-10-0-191-211 ~]$ service.
[ec2-user@ip-10-0-191-211 ~]$ sudo nano/usr/share/nginx/html/index.html
[ec2-user@ip-10-0-191-211 ~]$ l/index.html: command not found
[ec2-user@ip-10-0-191-211 ~]$ sudo nano /usr/share/nginx/html/index.html
[ec2-user@ip-10-0-191-211 ~]$
[ec2-user@ip-10-0-191-211 ~]$ sudo nano /usr/share/nginx/html/index.html
[ec2-user@ip-10-0-191-211 ~]$ y
-bash: y: command not found
[ec2-user@ip-10-0-191-211 ~]$ sudo nano /usr/share/nginx/html/index.html
[ec2-user@ip-10-0-191-211 ~]$ sudo systemctl restart nginx
[ec2-user@ip-10-0-191-211 ~]$ client_loop: send disconnect: Connection reset
