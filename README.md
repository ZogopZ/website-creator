# website-creator
A shell application that randomly generates websites and webpages.

# How to run
Open a terminal in the parent directory and type:
```sh
$./webcreator.sh root_directory text_file w p
```
website-creator is responsible for the following tasks:
1. Checks given arguments which must be exactly four. If not the application will return the following error message "Illegal number of parameters".
2. Checks if root_directory is an existing valid directory inside the parent directory.
3. Checks if text_file is a valid file containing 10.000 or more lines.
4. Checks if the last two arguments (website number ```w``` and page number ```p```) are integers greater than 3.
5. Checks if root_directory is empty and empties it if not.
6. For each website creates ```p``` number pages. The name of each page within a website contains a unique random number and thus each page has a unique name.
7. Creates ```w``` number websites and calculates how many internal and external links each page will contain and how many lines will be copied from the text_file. The internal and external links are selected randomly. All internal links that reference the page itself and duplicates are removed from the process.
8. Using the standard ```touch``` command the files are created and then the HTML headers are added.
9. A random internal or external link is chosen and a specified number of lines are being copied from the text_file to the page. Then the link is copied below. This process is repeated until all links are copied.
10. The HTML closing headers are then added and this process is repeated for all pages in all sites.
11. At the end of the script a check is performed whether each page has at least a link in other files referencing itself.