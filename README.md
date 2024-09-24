# ds6600_lab1
Lab 1 ds6600

# License Choice

I chose the GNU General Public License because it allows others to use and modify my code but does not allow them to modify that code and then enact a more restrictive license. If I hadn't provided a license I would be protected under general copyright and nobody would be allowed to use or modify my code at all. This would likely result in people being unwilling to fork or work with my code in any sense as they would not be protected by any license.

# Relevant .gitignore: 

.env

# Question 3 Answers:

**Meals on Wheels**
I recommend using a Virtual Machine for this use case. This is because the organization may have changing requirements, such as database type and storage capacity, and they also need to maintain isolation between different Meals on Wheels chapters. Each virtual machine can function as an independent system while being connected to the internet. Docker containers could also be a viable solution, as the frontend, backend, and databases can each run in separate containers, connected via a Docker network. However, Docker might not be ideal if there is a need to change databases between chapters. Virtual environments and the global environment are too simplistic and could lead to significant issues in setting up and managing environments across chapters.

**Legal Aid Justice Center**
I recommend using your global environment for this use case. Since they are only interested in the final product and not your code, using the global environment on your machine is perfectly acceptable. Although using a virtual environment could help with encapsulation and maintaining a clean workspace, anything beyond that, such as Virtual Machines or Docker containers, would be excessive and unnecessary in this scenario.

**Save The Children**
I recommend using Docker containers for this scenario. Docker containers natively support many Linux distributions, including Ubuntu, which resolves the issue of Python package compatibility. This machine learning model needs to be deployed by multiple people in potentially unstable environments, and Docker’s standardized build process ensures that the same container, and therefore the same model, is created every time for all deployments. While virtual machines might work, they would be too cumbersome and difficult to use, given the need for repeated deployments by different people. Virtual environments and the global environment would be far too simplistic, requiring each person deploying the model to be proficient with command-line tools and arbitrary commands, rather than just Docker commands.

**Swedish Python**
I recommend using a virtual environment, such as those provided by Pyenv and Pipenv, to select a Python version that is not in Swedish. While the global environment could be used, it would only allow you to have one Python version installed, preventing you from easily switching between the two versions. Docker and virtual machines would likely be overkill for this situation.

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

Python 3.12.3 (main, Sep 11 2024, 14:17:37) [GCC 13.2.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>>

# Question 5: 

Dockerhub link: https://hub.docker.com/u/wloving77 

# Question 6 Special Paste:

After the Creation, the cruel god Moloch rebelled:

    against the authority of Marduk the Creator.
    Moloch stole from Marduk the most powerful of all
    the artifacts of the gods, the Amulet of Yendor,
    and he hid it in the dark cavities of Gehennom, the
    Under World, where he now lurks, and bides his time.
