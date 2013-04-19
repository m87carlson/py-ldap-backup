This is a simple python (2.7) script that will backup the OpenLDAP database (as defined as backup_dir).

The output file, ldapdb.${DATE}.ldif is then compressed with bzip2

Finally, the script will remove any old backup files that are older than 28 days.

I run this during business hours with a cronjob:

10 9-17 * * * /usr/local/scripts/ldap_backup.py

