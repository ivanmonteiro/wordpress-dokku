# wordpress-dokku
Dokku is a small PaaS implementation, that allows deploys using git.

This repository was made to migrate an existing wordpress application to Dokku. 
The folder web shoud be replaced with the root folder of wordpress (the one containing index.php and config.php).
Usind Dokku this can be done with the command "dokku storage:mount app hostFolder:containerFolder"
Why?
Because wordpress changes core files during updates and wp-content when media is added to the website. This data should be outiside of the container or it would be lost if conteiner is missing.
