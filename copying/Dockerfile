FROM ubuntu

# update ubuntu
RUN apt-get update

#install C complier
RUN apt-get install build-essential -y

#create new directory to be the working directory
WORKDIR /app

# copy hello.c to the conatainer
COPY hello.c . 

#compile the hello.c to an executable
RUN gcc -o hello hello.c

# run the executable
CMD ./hello
