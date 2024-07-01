Staring:
sudo docker run -it --name website ubuntu sh -c 'while true; do echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website; done'

Fixing it:
sudo docker exec -it website bash
inside bash shell:
apt-get update
apt install curl
