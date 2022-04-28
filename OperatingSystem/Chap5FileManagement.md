# C5 File Management

# File Manager
> Controls every file in a system

### Efficiency Depends on:
- How system's files are organized (Sequential/Direct/Indexed Sequential)
- How files are stored (Contiguous/Non-contiguous/Indexed file storage allocation)
- How files are structured (fixed-length/variable length)
- How the files should be accessed (permissions)

### Responsibilities
- Track where each files are stored
- Determine where the file will be stored and how it will be stored
    - Tied to efficiency
        - Use available storage space efficiently
        - Provide efficient access to a file
- Allocate a file when the user has opened it, and record its use
- Deallocate a file when the user closed the file, and the file is returned to the storage
- Communicate the file's availability with other programs that request the file access and are waiting for the file to be available
- (kaki think eh notes dh) Track which permissions a file has

# Important Definitions ~~AKA Chim Words~~
- [Field](#field)
- [Record](#record)
- [File (Flat File)](#file-flat-file)
- [Database](#database)
- [Program Files](#program-files)
- [Data Files](#data-files)
- [Directory](#directory)

### Field
- A group of related bytes that can be identified by the user with name, type and size

### Record
- A group of related field together

### File (Flat File)
- A group of related record together that can be used by some softwares to generate reports

### Database
- Group of related files that are interconnected to give flexible access to users
- Appears to the file manager a type of a file

### Program Files
- Files that contains executable codes or instructions that can be runned

### Data Files
- Files that are only used to store data

### Directory
- Can think of a folder
- Contains a list of the program and data files, with their file name and attributes

### Every piece of computer software **IS** a file
### File manager treats all the files exactly the same, as far as storage is concerned, the usage of the file depends on the operating system

# Interacting With File Manager
- [Embedded Commands (Programs)](#embedded-commands)
- [Interactive Commands (User)](#interactive-commands)
- [Device Independence](#device-independence)

### Embedded Commands
- Issued by programs
- OPEN & CLOSE
    - Gives information of the accessibility of the file to the program invoking it
- READ & WRITE
    - I/O commands (does exactly as it reads)
- MODIFY
    - Special WRITE command that allows the data files to be appended/rewritten with records

### Interactive Commands
- Issued by user
- CREATE & DELETE
    - Deals with the system's knowledge of the file
- SAVE
    - When SAVE is used for the first time, the file is actually created
- OPEN NEW
    - When used within a program, implies that a file MUST be created
- OPEN ... FOR OUTPUT
    - Creates file by 
        - Making space for it in the directory
        - Finding space for it in the secondary storage
- RENAME
    - Allow user to change the file name of an existing file name
- COPY
    - Allow user to duplicate an existing file

### Device Independence
- Interface commands are designed to be device independent and easy to use
    - They do not need to have knowledge about low level stuffs like the physical memory address (cylinders, surface, sectors)
    - They do not need to have knowledge about the device medium (tape, disk, drive etc.)
    - They do not require knowledge about network
- Every logical command can be broken down into a sequence low level signals that
    - Triggers step by step actions performed by a device
    - Supervise progress of operation by testing the device's status
- Eg. READ command
    - MOVE read/write head to the cylinder
    - WAIT for search time (rotation delay)
    - Activate the appropriate head, READ the record
    - Send a flag indicating the device is free for processing another request
