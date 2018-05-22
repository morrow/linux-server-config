# Linux Server Config

## IP Address and SSH Port
[34.234.73.115](http://34.234.73.115)

786

## URL
[http://catalog.ninja](http://catalog.ninja)

## Software installed and configuration changes made
### Software installed
- `nginx 1.10.3`
- `pip 10.0.1`
- `postgresql 9.5.12`
- `gunicorn 19.8.1`

### Configuration changes made
- Update securiy group policy on Route 53 to allow for incoming TCP connections on 80, 443, 123, and 786
- Create user group `web`
- Add `ubuntu` to `web` group
- Create /var/www folder owned by `ubuntu.web`
- Add configuration for nginx at `/etc/nginx/sites-enabled/catalog`
- Add unit file for systemd at /etc/systemd/system/catalog.service for WSGI
- Create user `grader`
- Add `grader` user to `sudoers`
- Generate SSH keypair for user `grader`
- Add SSH public key to /home/grader/.ssh/authorized_keys
- Update ufw to allow only select ports
- Enable ufw
- Create Postgres user `catalog` using psql
- Update password for Postgres user `catalog`
- Create database `catalog`
- Update `app.py` and `database_setup.py` to connect to Postgresql with `catalog` user and password

### Third Party resources used
- [https://aws.amazon.com/route53](https://aws.amazon.com/route53) for DNS management and domain name registration services.
- [https://aws.amazon.com/ec2](https://aws.amazon.com/ec2) for virtual server provisioning and management.
- [https://github.com/morrow/catalog](https://github.com/morrow/catalog) for application logic.

