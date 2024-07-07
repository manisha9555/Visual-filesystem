# Visual File Management System
# Table of Contents

Defining the Problem Statement:
Selecting the Data Structure:
# Execution of Solution:
Algorithms
print_tree(root, prev_struct)
print_ls(node=pwd->child)
pwd_str(root, pwd)
find_names(root, pwd, name)
find_on_pwd(pwd, name)
find_node(root, pwd, path)
cd(root, pwd, path)
create(root, pwd, path, type)
remove(root, pwd, path)
dupl(root, pwd, src_path, dst_path, keep)
cat(root, pwd, path)
edit(root, pwd, path)
chmod(root, pwd, path, new_modes)
Dry Run
Defining the Problem Statement:
Data on every Operating System is stored in a hierarchical file system constituted of directories and subdirectories beneath them. A file management system is the program used to arrange these files, move them, and create / delete them. This take care of how the files are organized rather than how they are stored.

# The key features are to:

Create, modify, move, copy, delete and other file operations.

Add or edit basic metadata.

Selecting the Data Structure:
Trees would be the best suited data structure to implement this because nodes and leaves of the tree resemble the directories and sub-directories containing files in them.

A binary tree cannot do the job here as it restricts to only having two children. N-ary Tree should be implemented solve this. Since we do not know what will be the value of n, each node cannot have a fixed child links.



But if we think this as keeping the contents of a directory as a linked list and only storing the first child’s address, then each node can have exactly 2 links. This makes it possible to use algorithms of Binary Tree as well.



There is also a need to traverse upwards to its root. This can be solved by creating another link with the parent directory. Although this technically becomes a Graph, but implementation will be like a binary tree in a broad level and like linked list in a directory level.



# Execution of Solution:
The execution is very much inspired from Linux shell. The program resembles the shell which contains the present working directory on left and prompt at end. The user can use following commands just like in the Linux shell. Some key commands are:

cd - to navigate through directories

ls - to list the files and sub-directories in a directory

tree – to view a tree structure of what is inside a directory until the last file

mkdir – to create a new directory

touch – to create a new file

edit – to edit the file contents

rm / rmdir – to remove a file / directory respectively

cp / mv – to copy / move a file or directory respectively

find – to find files or directories# Visual-filesystem
