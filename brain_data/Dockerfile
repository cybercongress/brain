
#os
FROM ubuntu:18.04

#update
RUN apt update && apt upgrade -y

#dependes
RUN apt install -y git nano npm nodejs curl

#meteor
RUN curl https://install.meteor.com/ | sh

#brain
RUN cd /opt && mkdir brain-bin && mkdir settings && git clone https://github.com/cybercongress/brain.git

#initialize meteor
RUN cd /opt/brain && git checkout master && meteor npm install --allow-superuser && meteor update --allow-superuser

CMD cd /opt/brain && meteor --settings /opt/settings/settings.json --allow-superuser