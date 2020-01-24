FROM ubuntu

RUN apt-get update

RUN apt-get install -qy python3\
    python3-pip\
    git\
    virtualenv
RUN mkdir ./workspace &&\
    cd ./workspace &&\
    git config --global user.name yourusername &&\
    git config --global user.email youremail@email.com &&\
    git clone https://github.com/Rypeur/H3-Big-data.git

COPY . /workspace
WORKDIR ./workspace

RUN pip3 install -r requirements.txt

EXPOSE 8000

CMD [ "jupyter", "notebook", "--ip=0.0.0.0", "--port=8000", "--allow-root"]