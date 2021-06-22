# squid-cache
squid-cache for yum and dnf

This is squid configured for caching rpm packages.

The stack-file and config are for runing with docker swarm

For use with traefik v2 wich is configured in the stack you need the following lines in traefik-stack.yml
...
    ports:
...
      - "3128:3128" # Open Squid Port
    command:
...
      - --entrypoints.squid.address=:3128
...

