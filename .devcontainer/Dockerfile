# Python 3.7 image
FROM python:3.7-buster

ARG USER=alekssro
ARG USER_ID=1000
ARG GROUP_ID=1000

# RUN userdel -f root &&\
    # if getent group root ; then groupdel root; fi &&\
RUN groupadd -g ${GROUP_ID} ${USER} &&\
    useradd -l -u ${USER_ID} -g ${USER} ${USER} &&\
    install -d -m 0755 -o ${USER} -g ${USER} /home/${USER}

USER ${USER}

# Packages that we need 
COPY requirements.txt /app/
WORKDIR /app

# instruction to be run during image build
RUN pip install -r requirements.txt

# save color scheme
RUN echo "export PS1='[\A] \[\033[38;5;198m\]\u@\h:\[\033[00m\]\[\033[0;92m\]\w:\[\033[00m\] '" >> ~/.bashrc
RUN echo "LS_COLORS=$LS_COLORS:'di=1;33:' ; export LS_COLORS" >> ~/.bashrc 
RUN echo "export GCC_COLORS='error=01;31:warning=01;33:note=01;36:caret=01;37:locus=01:quote=01'" >> ~/.bashrc

# Copy all the files from current source directory(from your system) to

# Docker container in /app directory 
COPY . /app

# Specifies a command that will always be executed when the  
# container starts.
# In this case we want to start the python interpreter

ENTRYPOINT [“python”]

# We want to start main.py file. (change it with your file name) 