# htaccess-hacks
Just a collection of hacks for your .htaccess file to improve server security.

You can test some of these here: https://htaccess.madewithlove.be

# Uploads Protection
You can copy / paste the code from the uploads-protection file into a .htaccess and place it in your /wp-content/uploads folder. This will prevent .php files from executing that somehow ended up in your uploads folder (and there should NEVER be a .php file in your /uploads folder).

# Note on all-inkl with PHP Version 8.0
all-inkl no longer allows to set the memory_limit as well as the max_execution_time via the .htaccess if your domain is set to PHP Version 8.0 or higher (it only did so until 7.4).
To increase the memory_limit and the max_execution_time for your domain, create a .user.ini in the root folder that your domain points to and enter the following:

```
memory_limit = 256M
max_execution_time = 320
```

This will (after a minute or so) change the PHP variables to the values you set.
