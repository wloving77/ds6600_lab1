# ds6600_lab1
Lab 1 ds6600

# License Choice

I chose the GNU General Public License because it allows others to use and modify my code but does not allow them to modify that code and then enact a more restrictive license. If I hadn't provided a license I would be protected under general copyright and nobody would be allowed to use or modify my code at all. This would likely result in people being unwilling to fork or work with my code in any sense as they would not be protected by any license.

# Relevant .gitignore: 

.env

# Question 3 Answers:

**Meals on Wheels**: I recommend a Virtual Machine for this use case. I recommend this because they have potentially changing requirements (Database Type and Storage Amount) but also want to have isolation by chapter of Meals on Wheels. These virtual machines will act as their own independent systems and can all be connected to the internet. I also think Docker Containers would be a decent use case here as the frontend, backend, and databases can each be their own containers and they can be connected via a docker network. The only problem with docker is the potential requirement for changing databases between chapters. Virtual environments and the global environment are too simple and leave a ton of potential for issues and environment setting up between chapters. 

**Legal Aid Justice Center**: I recommend simply using your global environment for this use case. Because they don't want your code and just care for the final product using your machines global environment is perfectly fine. There is nothing wrong with using a virtual environment simply for encapsulation and cleanliness of code but anything past virtual environment is pure overkill in this scenario. Virtual machines and Docker containers don't really provide any convenience here and are thus unnecessary.

**Save The Children**: I recommend a Docker Container in this scenario. Docker containers natively support many distributions of Linux including Ubuntu so the python package requirements are solved there. This ML Model also has to be deployed by multiple different people throughout potentially collapsing cities which Docker's standardized build step allows creating the same container and thus the same model every time for all deployments. Virtual Machines might work but because this model needs to be cloned and deployed repeatedly by different people it is likely a virtual machine software would be too cumbersome and difficult to use. Virtual environments and the global environment would be far too simple and would essentially require every person deploying this model to be comfortable on a command line with arbitrary commands and not just docker based commands.

**Swedish Python**: I would recommend a Virtual Environment with something like Pyenv and Pipenv to choose a python version that is not written in Swedish. The global environment could work but you'd have to have only one version of python which would not allow you to simultaneously hot swap between the two versions. Docker and Virtual machines would likely just be overkill in this scenario. 

# Question 4 Answers: 

**Dockerfile:**

FROM ubuntu:latest

RUN apt-get update && apt-get install -y python3

CMD ["python3"]

**Docker Build Terminal Output:** 

[+] Building 37.7s (7/7) FINISHED                                                                                                                                                                                                                                 docker:default
 => [internal] load build definition from Dockerfile                                                                                                                                                                                                                        0.0s
 => => transferring dockerfile: 277B                                                                                                                                                                                                                                        0.0s
 => [internal] load metadata for docker.io/library/ubuntu:latest                                                                                                                                                                                                            0.7s
 => [auth] library/ubuntu:pull token for registry-1.docker.io                                                                                                                                                                                                               0.0s
 => [internal] load .dockerignore                                                                                                                                                                                                                                           0.0s
 => => transferring context: 2B                                                                                                                                                                                                                                             0.0s
 => [1/2] FROM docker.io/library/ubuntu:latest@sha256:dfc10878be8d8fc9c61cbff33166cb1d1fe44391539243703c72766894fa834a                                                                                                                                                      8.8s
 => => resolve docker.io/library/ubuntu:latest@sha256:dfc10878be8d8fc9c61cbff33166cb1d1fe44391539243703c72766894fa834a                                                                                                                                                      0.0s
 => => sha256:dfc10878be8d8fc9c61cbff33166cb1d1fe44391539243703c72766894fa834a 1.34kB / 1.34kB                                                                                                                                                                              0.0s
 => => sha256:77d57fd89366f7d16615794a5b53e124d742404e20f035c22032233f1826bd6a 424B / 424B                                                                                                                                                                                  0.0s
 => => sha256:b1e9cef3f2977f8bdd19eb9ae04f83b315f80fe4f5c5651fedf41482c12432f7 2.30kB / 2.30kB                                                                                                                                                                              0.0s
 => => sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6 29.75MB / 29.75MB                                                                                                                                                                            1.2s
 => => extracting sha256:dafa2b0c44d2cfb0be6721f079092ddf15dc8bc537fb07fe7c3264c15cb2e8e6                                                                                                                                                                                   1.2s
 => [2/2] RUN apt-get update && apt-get install -y python3                                                                                                                                                                                                                 27.7s
 => exporting to image                                                                                                                                                                                                                                                      0.4s 
 => => exporting layers                                                                                                                                                                                                                                                     0.4s 
 => => writing image sha256:aaf550f476f8d21313033b5474e6661cd1fcc25723e5c9cd428f4c19a91d243a   

 **Output From Docker Run:**

$ docker run -it lab1-image
Python 3.12.3 (main, Sep 11 2024, 14:17:37) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>



# Question 5: 

Dockerhub link: https://hub.docker.com/u/wloving77 

