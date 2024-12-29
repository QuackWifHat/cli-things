# Utilization of Linux tool 'dd'
Taking an .img file and burning it onto an sd card.
```
# bs=4M is used to make things go faster (apparently | source: https://askubuntu.com/questions/179437/how-can-i-burn-a-raspberry-pi-image-to-sd-card-from-ubuntu) 
sudo dd if=/home/username/path/to/image-file.img of=/path/to/dest status=progress bs=4M
```
