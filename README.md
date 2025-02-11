# Virtual File System in C

This project implements a virtual file system in C that simulates basic shell operations such as creating directories, writing files, listing contents, etc.

## Authors

- Marc Nadal Sastre Gondar
- Joaquín Esperon Solari  
- Martí Vich Gispert

## Description

The project implements a virtual file system with functionalities similar to those of a Unix/Linux shell. It allows managing files and directories on a virtual device, offering basic operations such as:

- Creating directories and files
- Writing and reading content
- Listing directory contents
- Modifying permissions
- Deleting files and directories
- Retrieving file/directory information

## Implemented Commands

- `mi_mkdir`: Creates a new directory
- `mi_touch`: Creates a new file
- `mi_ls`: Lists directory contents (implemented with a detailed format similar to `ls -l`)
- `mi_cat`: Displays the content of a file
- `mi_chmod`: Modifies the permissions of a file or directory
- `mi_stat`: Displays detailed information about a file or directory
- `mi_rm`: Deletes a file
- `mi_rmdir`: Deletes a directory
- `mi_rm_r`: Recursively deletes directories and their contents

## File System Structure

The file system is organized into:

- Superblock
- Bitmap
- Inode array
- Data blocks

## Technical Features

- Block size: 1024 bytes
- Unix-like permission system (read, write, execute)
- Metadata management (creation, modification, access dates)
- Support for links
- Semaphore implementation for concurrency control

## Compilation and Usage

1. Compile the project:

```sh
make
```

2. Create and mount the file system:

```sh
./mi_mkfs <device_name> <size>
```

3. Usage examples:

```sh
./mi_mkdir <device_name> <permissions> <path>
./mi_ls <device_name> <path>
./mi_touch <device_name> <permissions> <path>
./mi_cat <device_name> <path>
```

## Additional Notes

- The `mi_ls` command always displays detailed information (similar to `ls -l`).
- The system implements error control and informative messages.
- A color-coded output system is used for better visualization.
- Includes protection against common errors and argument validation.

## Limitations

- The `mi_touch` command has not been implemented independently (`mi_mkdir` is used instead).
- Some advanced file system functionalities are not implemented.

## Requirements

- C compiler
- Unix/Linux operating system
- Make

## License

This project is for educational use and is available for study and modification.

