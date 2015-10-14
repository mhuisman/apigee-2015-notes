# NodeJS and Docker microservices 

Benefits of the monolith
* Straightforward
* Deployment is (comparatively) easy
* Scaling model is simple: add better hardware, add more boxes to pool 

Deployment process significant
* creating server environments time consuming, laborious, expensive
* limited practically
* staged pipeline include some fixed # of server environments (dev->stage->prod)
* Improved with virtualization (vagrant, puppet, chef) but still burdensome

Adverse impacts
* significant cost/investment makes releases expensive and significant, slower/fewer
* inhibits continuous delivery
* scalability is sub optimal - limits on upscaling, outscaling expensive and impractical
* Large codebase difficult to maintain and extend
* high cognitive overhead leads to burnout

Microservices a form/subset of SOA
* implies containerization
* by heterogeneous client pool leads to emphasis on APIs not applications
* improvements in distributed technology improve our ability to be effective

Consequences of APIs
* desirable to evolve, deploy scale independently
* potential for reducing codebase complexity (hah!)
* potential for reduced developer friction; less integration, more focus, own delivery cadence

Yay Docker (dum ba-da dut daaaaah!)
* What is the difference between Docker and a VM instance? (pic)
* VM has entirety of guest OS deployed
* Docker has only stripped down kernel; only the container profile that the user configures

Yay Node (ta rum ta tum-tum-tum)
* Lightweight server processes
* highly scalable - asynch IO, no special OS requirements for deployment
* lightweight for development

Recommendation for teams (opinions!)
* 'Java is oriented towards more complicated problem sets'
* 'Node microservices should be small, easy to reason about, test and debug'
* Use polyglot (i.e. not node) workers for computationally heavy callouts
* use native Node as the common REST API layer.  orchestration layer? (mkh)

Practical set
docker-machine create --driver <driver-name> <machine-name>
docker-machine ls 
eval "$(docker-machine env <machine-name>)"
docker-machine stop|start <machine-name>
docker-machine ssh <machine-name>
docker run --rm <image> [cmd] (non-interactive mode)
docker run --rm -it <image> [cmd] (interactive mode)
docker pull node (pull latest node)
docker run --rm node node -v; npm -v (run container and display node/npm version)
