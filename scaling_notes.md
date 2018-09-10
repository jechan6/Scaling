## Scaling server
    + Improve cpu speed, replace with a better cpu
    + Buy more hardware, more servers to handle request
## Factors for slow application
    + Main reason is database
    + All data either lives in computer's ram or hard disk
    + Persistence data means slow access and writing
    + Non-persistence means fast access and writing(RAM)
## RAM
    + RAM is like a cache
    + Data in a disk could be written to a RAM if the size is sufficient
    + If there are more data than a ram could fit, only the most active data is put on the ram

## Scaling out
    + Scaling out a database is complicated, scaling a server/rails server is simple
    + Break up work between multiple server
    + All server connected and talks to one database.
    + User talks to a load balancer that talks to three machines. Picks one machine randomly, Copies user's entire request and make the same request to the machine.
    + Load balancer's work is very simple, copy the request and pass it over to the machine.
    + User and rails machine does not know about each other when using a load balancer
    + Load balancer receives a reponse from the machine and pass the response onto the user
    
