# tacsplus Docker Compose
Open tacacs project:

Three files should be mounted, 
tac_plus.conf → containing the user and group information, and the command authorization.
passwd → containing the password hash of each user 
tac_plus.acct → containing the logs of accounting and authorization commands.
As the above three files are important, so they should be mounted in a volume or file somewhere, 
otherwise, they will be removed when the docker container is stopped.

To check accounting log you can run below command
tail -f /var/log/tac_plus.acct
Or send it to your log collector.
