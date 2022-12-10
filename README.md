# disaster_recovery-jenkins
## Rescuing a Crashing Jenkins instance
***
1.  Install your thinBackup plugin
2.  Create your backup directory in the backend of your jenkins master machine
3.  make sure the backup directory is on a different user but with jenkins having access to that directory.
4.  Configure your thinBackup plugin according to the parameters that you wish. 
5. Once you’ve saved and done, you click on restore, and you choose the date in which you performed the backup and then you click on restore. _It will then pull down all the jobs, plugins and other configuration files that was backed up into your backup directory._