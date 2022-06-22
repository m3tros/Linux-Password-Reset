# Linux-Password-Reset


## Stop grub boot
To abort grub boot, press the `shift` key. 
 

<p align="center"> 
  <img src="https://user-images.githubusercontent.com/107058068/175105442-4c6bab28-9c1c-43aa-9f53-0d6cf797d073.png" alt="Linux-Password-Reset">
</p>

## Editing boot options
Then press the `e` key to go to the boot settings editor.
 

<p align="center"> 
  <img src="https://user-images.githubusercontent.com/107058068/175105519-bdf5aa01-004e-4bb6-9f5e-60efabfdc7f6.png" alt="Linux-Password-Reset">
</p>


Now you need to find the line indicated below. 
 

<p align="center"> 
  <img src="https://user-images.githubusercontent.com/107058068/175105914-536cd7d3-55ed-48d3-a382-418eb5898135.png" alt="Linux-Password-Reset">
</p>

At the end of this line, we need to enter:
```
splash $vt_handoff single init=/bin/bash
```
If you already have the `splash $vt_handoff` line, then you just need to add `single init=/bin/bash`.<br>
After you have finished writing, press the key combination `Ctrl+X`.

## Bash

 

<p align="center"> 
  <img src="https://user-images.githubusercontent.com/107058068/175107713-c968fedd-5e8b-49bc-9194-57ddbbb3185d.png" alt="Linux-Password-Reset">
</p>


You have started bash now you need to enter the command below:
```bash
passwd
```
Or for a specific user:
```bash
passwd <username>
```
After that, the password will be changed. To reboot, enter the command below:
```bash
reboot -f
```
It is possible that you will encounter errors below are the errors and their solutions.




## Authentication token manipulation error
 
 <p align="center"> 
  <img src="https://user-images.githubusercontent.com/107058068/175108090-07abc23c-01da-4e03-b4a7-157ca6211543.png" alt="Linux-Password-Reset">
</p>
 
It's a mistake `Authentication token manipulation error` fix this error by entering below commands:
```bash
sudo mount -o remount,rw /
```

Then enter the commands again:
```bash
passwd
```
Or for a specific user:
```bash
passwd <username>
```
After that, the password will be changed. To reboot, enter the command below:
```bash
reboot -f
```

 
