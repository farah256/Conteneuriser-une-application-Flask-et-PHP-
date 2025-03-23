# Image de base
FROM python:3.8-buster

# Mainteneur
LABEL Mainteneur="Salmi Farah farah.salmi02@gmail.com"

# Ajout du code source 
COPY student_age.py /
COPY requirements.txt /

# Installer les prérequis
RUN apt update -y && apt install python3-dev libsasl2-dev libldap2-dev libssl-dev -y
RUN pip3 install -r /requirements.txt

# Données persistantes
VOLUME [ "/data" ]

# Exposer le port de l'API
EXPOSE 5000

# Commande de démarrage
CMD ["python3", "./student_age.py"]