AWS Setup (t2.xlarge) (with open network) 16gb ram
Associate Elastic IP

....

wget https://github.com/ahmetoner/whisper-asr-webservice/archive/refs/heads/main.zip

sudo apt-get install unzip

unzip main.zip

cd whisper-asr-webservice-main/

sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt update

sudo apt install python3

sudo apt install ffmpeg

python3 --version

sudo apt install python3-pip

after poerty install

nano ~/.bashrc

export PATH="/home/sammy/.local/bin:$PATH"

source ~/.bashrc

build poetry before running

permission denied
sudo chown -R ubuntu /root
sudo chown -R ubuntu /root/
sudo chown -R ubuntu /root/*

poetry run gunicorn --bind 0.0.0.0:9001 --workers 1 --timeout 0 app.webservice:app -k uvicorn.workers.UvicornWorker --daemon
