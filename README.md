# Analysis-of-the-Disk-Structure-using-Sleuth-Kit
## AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

## DESIGN STEPS:
### Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

### Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

### Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

## PROGRAM:
Sleuth Kit Disk Analysis Commands

✅ Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:
```
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```
## OUTPUT:

# mmls
```
mmls disk.dd
```
# fls
```
fls -f fat -o 0 disk.dd
```

<img width="543" height="252" alt="image" src="https://github.com/user-attachments/assets/421566ce-da79-4972-9a01-f268c2443a8d" />

<img width="1027" height="645" alt="image" src="https://github.com/user-attachments/assets/1c6755ea-d7bf-4a90-8a48-de65dd16e7e2" />

<img width="579" height="244" alt="image" src="https://github.com/user-attachments/assets/2e68e41d-f84c-411c-83cf-4ec58bd5fce5" />

<img width="510" height="383" alt="image" src="https://github.com/user-attachments/assets/d0e18113-e79a-4f51-946c-fa6aa9f62632" />


## RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
