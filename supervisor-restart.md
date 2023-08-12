ps -A | grep "laravel-worker"
sudo supervisorctl status
sudo supervisorctl stop laravel-worker:*
ps -ef | grep supervisord
sudo kill -3 pid
sudo supervisorctl status
sudo supervisord -c /etc/supervisor/supervisord.conf
sudo supervisorctl status
