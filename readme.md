# Example
```
docker run -i --rm \ 
  -e TLS=YES \
  -e mailhub=smtp.gmail.com:587 \ 
  -e AuthUser=xxx@gmail.com 
  -e AuthPass=xxx \ 
  philoles/mail \
  sh -c 'df -h > /tmp/mail_report.log && free -m >> /tmp/mail_report.log && mail -s "$HOSTNAME disk and RAM report" xxx@gmail.com < /tmp/mail_report.log'
```
