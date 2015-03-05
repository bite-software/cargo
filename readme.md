#Cargo

Creating `Docker` containers are one thing, but deploying them to the server for the purpose that each of them will run as a uniquely contained application with its dendencies, is the other side of the coin. Not only do we fill our Containers - but we need the ability to deploy our containers as cargo, even if our system is offshore.
	
	~/ cargo push my-app-container

Project targets, as far as we know it:

* set up a minimal clean linux distro
* spec out the cargo API and how this can be managed, either through a `ruby` app; `shell` script or even just via the simplicty of Github `webhooks`, where a `git push` of our docker container will automate the process of our linux server pulling the container itself and deploying it into service
* create a sample docker container

As I write this, rather than naming it _cargo_ the image of a container being flown in via helicoptor, and dropping off its load to a moving containship seems to fit the description better .. whatever that word is maybe describes this first sketch better.

####Criticism and concerns

* Does this concept swallow up huge server resources?
* How does one manage load balancing?
* Should one container manage multiple 'nested' containers