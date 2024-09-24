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

