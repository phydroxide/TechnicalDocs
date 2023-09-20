```
 gcloud compute instances create kali \
--machine-type=e2-standard-8 \
--network-interface=subnet=<subnet>,no-address \
--image-family=debian-11 --image-project=debian-cloud \
--boot-disk-size=200GB \
--zone us-central1-a
```

```
sudo apt-get install wget
wget https://archive.kali.org/archive-key.asc
sudo cp archive-key.asc /etc/apt/trusted.gpg.d/
```

```
echo "deb http://http.kali.org/kali kali-rolling main contrib non-free" >> /etc/apt/sources.list
apt-get -y update
```

```
sudo apt-get install screen
sudo apt-get install python3-venv
sudo apt-get install kali-linux-everything
```


Maxmind
https://dev.maxmind.com/geoip/updating-databases?lang=en
```
apt-get install python3-pip
pip install geoip2
```
https://www.maxmind.com/en/accounts/634099/geoip/downloads


```
curl '<url>' -o GeoLite2.gzip
tar -xzf GeoLite2.gzip
find ./GeoLite2-* -name *.mmdb -exec sudo cp {} /usr/share/GeoIP/ \;
```

VNC

```
sudo apt update && sudo apt install -y kali-desktop-xfce

sudo apt update && sudo apt install -y lightdm

sudo update-alternatives --config x-session-manager

vncserver -geometry 4096x2160 -geometry 1920x1080 -geometry 1280x1024
```

Bigger Hardware
```
gcloud compute instances set-machine-type kali --machine-type=e2-custom-4-8192
gcloud compute instances set-machine-type kali --machine-type=e2-standard-8
gcloud compute instances set-machine-type kali --machine-type=e2-micro
```
