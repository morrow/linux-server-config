# Linux Server Config

## i. IP Address and SSH Port
[34.234.73.115](http://34.234.73.115)

786

## ii. URL
[http://catalog.ninja](http://catalog.ninja)

## iii. Software installed and configuration changes made
### Software installed
- `nginx 1.10.3`
- `pip 10.0.1`
- `postgresql 9.5.12`

### Configuration changes made
- Create user group `web`
- Add `ubuntu` to `web` group
- Create /var/www folder owned by `ubuntu.web`
- Add configuration for nginx at `/etc/nginx/sites-enabled/catalog`
- Create user `grader`
- Add `grader` user to `sudoers`
- Generate SSH keypair for user `grader`
- Add SSH public key to /home/grader/.ssh/authorized_keys
- Create Postgres user `catalog` using psql
- Update password for Postgres user `catalog`
- Create database `catalog`
- Update `app.py` and `database_setup.py` to connect to Postgresql with `catalog` user and password

### Third Party resources used
- [https://aws.amazon.com/route53](https://aws.amazon.com/route53) for DNS management and domain name registration services.
- [https://aws.amazon.com/ec2](https://aws.amazon.com/ec2) for virtual server provisioning and management.
- [https://github.com/morrow/catalog](https://github.com/morrow/catalog) for application logic.


    
 
