**Author:** liyanqing.1987@163.com    
**Version:** V1.0 (2024.07.08)    
    
# What is “safe_rm”?
 
 `safe_rm` is a secure data deletion tool, which works exactly the same as `rm`. It can be referenced in an alias manner or directly replace the system's rm command.

# Requirements

- Linux
- Python 3

# Quick Start

1.  use as alias    

     `[user@host ~]# alias rm=“/***/safe_rm“`    
     `[user@host ~]# rm ***`    
     
     <img src=“./alias_demo.gif” alt=“use as alias”>

2.  replace system rm    

     `[root@host ~]# which rm`    
     `/usr/bin/rm`    
     `[root@host ~]# mv /usr/bin/rm /usr/bin/system_rm`    
     `[root@host ~]# cp safe_rm /usr/bin/rm`    


# Configuration

 It consists of two utilities: `rm-p` and `protect`. The latter one is to help you protect files.

 For example, you have a file called `important_file` and it is `protect`ed by `.important_file.rm-protection`. `rm-p` will recognize that `important_file` is protected and prompt to ask you a question stored in `.important_file.rm-protection`. `rm-p` will only proceed if you get the answer right.

 See it in action:

 ![Basic usage](https://ooo.0o0.ooo/2017/02/03/58943760b76ed.gif)

 It will also prevent you from deleting a directory with `protect`ed file(s) inside.

# Demo