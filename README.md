# disaster_recovery-jenkins
## Rescuing a Crashing Jenkins instance
***
There are at least 2 ways this can be done through the UI. You can use the thinbackup plugin or the job import plugin technique. Secure copying through the backend is another option. 
### A. Using Thinback up technique
1.  Install your thinBackup plugin
2.  Create your backup directory in the backend of your jenkins master machine
3.  Make sure the backup directory is on a different user but with jenkins having access to that directory.
4.  Configure your thinBackup plugin according to the parameters that you wish. 
5. Once you’ve saved and done, you click on restore, and you choose the date in which you performed the backup and then you click on restore. _It will then pull down all the jobs, plugins and other configuration files that was backed up into your backup directory._

### B. Job Import Plugin Technique
1. Install the job import plugin on the server that you want to import to. Also ensure that all necessary dependencies are installed alongside.
2. Configure the plugin and supply url of source and authentification information.
3. You will be able to view files/jobs available to be copied on source machine.
4. Select file of interest and copy
### C. Secure copying via scp file transfer protocol
This is especially useful if you do not have access to the front end plugins. You log into the backend. You can just either run your commands directly or create a shell script to run scp commands from source to destination machines. Furthermore you can configure a cron job to periodically copy files across your machines.