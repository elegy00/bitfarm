# Vision Bitfarm

The bitfarm is an autonomous AI based softwarefactory that continues pushing my projects ahead:
* Implementing roughly defined new features
* Testing and verifying changes made to the application
* Upholding softwre engineering best practices and good code standarts

## Runtime
The bitfarm should run within k3s on ubuntu and run as independent as possible. It should start small and be extensible and become more refined with learnings along the way. As LLM a local LLM will be used to keep the full control over the development loop.
The bitfarm should be deployed itself similar to the recing application through github in k3s and in best case scenario can run the application fully internally to test it.

## Sample target project
In [Recing](../../recing/) is a sample project that would be the first candidate to continue on with development. It contains some rough understanding how AI has built applications so far

## Start simple and stupid
Start in as lightweight factory mode as possible:
### MVP
* Deploy the bitfarm container that has a single github repository configured with access to interact with it (github CLI / git)
* The bitfarm container has a Harness installed & configured
* The bitfarm has a loop to process tasks described in a folder in the repository

### Follow-up feature candidates
* Web UI to administrate various repositories / projects
* Task handling through github actions
* Run the application as subcontainers in k3s so the tested application is fully isolated from the 
* Various different workers on the bitfarm: Implementer, Architect, UX Engineer, that do not just implement new features but improve the quality of various parts

## LLM
Will be accessed similar to the recing project through the LAN, as Harness PI (pi.dev) will be used.