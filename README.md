Use system hostname within matlab.  The following creates a hostname variable within matlab and populates it with the systems computer name (generated from the system call hostname).  It then uses strcat and strjoin to create the following command string for execution later ```saveString = "save data/$hostname"``` where $hostname is the pc name.

```[~,hostname] = system('hostname');
matts = strcat({'save data/'},hostname);
saveString = strjoin(matts)```
