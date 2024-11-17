# [**Shell 01**](https://github.com/vinislima/42sp_piscine_shell01)

> The "Shell 01" project from the 42 school focuses on advanced shell scripting skills. It consists of exercises that develop proficiency in Unix commands and scripting logic, such as listing user groups, finding and counting files, extracting MAC addresses, and manipulating text output. Students are also challenged with creative tasks, like creating files with specific names and performing arithmetic operations using custom numeral systems. The project emphasises careful problem-solving, strict syntax adherence, and collaboration among peers while reinforcing core shell scripting concepts.
> 

The main shell commands introduced in the **Shell 01** project are:

- **`id`** - Retrieves the groups associated with a specific user and formats them as a comma-separated list.
- **`find`** - Searches the current directory and its subdirectories for files meeting certain criteria, such as .sh file extensions, and extracts their names without extensions.
- **`wc`** and **`find`** - Combined to count files and directories recursively within a directory tree.
- **`ifconfig` or `ip`** - Extracts and displays the MAC addresses of network interfaces.
- **Complex file handling** - Creates files with unconventional names, testing the ability to handle special characters.
- **`ls` with filters** - Skips every other line in directory listings to filter output.
- **`cat`, `sort`, and `pipes`** - Combines commands to manipulate and transform text files, such as reversing and sorting logins in specific ranges.
<details>
	<summary>Exercises:</summary>

- [ex01:](https://github.com/vinislima/42sp_piscine_shell01/tree/main/ex01)
    
    ```bash
    id -Gn $FT_USER | tr ' ' ',' | tr -d '\n'
    ```
    
- [ex02:](https://github.com/vinislima/42sp_piscine_shell01/tree/main/ex02)
    
    ```bash
    find . -type f -name "*.sh" | sed 's|./||; s|\.sh$||' | xargs -n 1 basename
    ```
    
- [ex03:](https://github.com/vinislima/42sp_piscine_shell01/tree/main/ex03)
    
    ```bash
    find . | wc -l
    ```
    
- [ex04:](https://github.com/vinislima/42sp_piscine_shell01/tree/main/ex04)
    
    ```bash
    ifconfig | grep ether | awk -F' ' '{print$2}'
    ```
    
- [ex05:](https://github.com/vinislima/42sp_piscine_shell01/tree/main/ex05)
    
    ```bash
    42
    ```
</details>