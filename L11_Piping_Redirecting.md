First off, experiment with saving output from various commands to a file. Overwrite the file and append to it as well. Make sure you are using a both absolute and relative paths as you go.

`$ ls /etc | tail -n 20 > output.txt`

`$ ls /etc | head -n 20 >> output.txt`

Now see if you can list only the 20th last file in the directory /etc.

`$ ls /etc | tail -n 20`

Finally, see if you can get a count of how many files and directories you have the execute permission for in your home directory.

`ls -l | tail -n +2 | cut -d ' ' -f 1 | egrep '[d,-]..x' -c`

