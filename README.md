# _p templates

_p templates are project related .md files trying to solve @todo lies, human memory leak, and more... 


## Installation

Go to the root directory of your current project
```bash 
cd /path/to/project
```

Clone the repository into a folder named `._p`.
```bash
git clone https://github.com/0kyn/_p.git ._p-templates
```

If you don't want _p-templates to be a git submodule of your current project, you should only clone the master branch of the repository, without keeping `.git` directory.
```bash
git clone --depth=1 --branch=master https://github.com/0kyn/_p.git ._p
rm -rf ._p/.git
```

Go to `._p`
```bash
cd ._p
```

### Structure example

projects/  
├─ projectA/  
│  ├─ **._p**/  
│  ├─ node_modules/  
│  ├─ public/  
│  ├─ src/  
│  ├─ vendor/  
│  ├─ .gitignore  
│  ├─ composer.json  
│  ├─ package.json  
│  ├─ README.md  
├─ projectB/  
├─ projectC/  

You might also want to add `._p` directory to your root `.gitignore` file, in the case where you store sensitive informations in these files and/or your repository is going to be public.

## Markdown Files

- `_bugs.md`    : Describes tricky bugs and how you solved it
- `_memo.md`    : Uses to store temporary notes
- `_todo.md`    : Lists tasks per module, note some features ideas, enhancements, usefull resources...
- `_tools.md`   : Uses as a reminder for command line you need to run regularly (npm docker composer)
- `_stack.md`   : Describes the technical stack, environments... and some keywords

## Usage

`_bugs.md` entries are never removed so as to keep tracks of issues and fixes.

Unlike`_memo.md` which is more like a "notepad on the fly" or a draft for ephemere things to remember. I actually never commit this file.

`_todo.md` is cleaned up *Tasks* and *Needs* once completed, tested, approved and run in production. The *Planning* is also updated when new deadlines come. *Misc.* are potential enhancements, features that could stand into *Tasks* later.

`_tools.md` When some tools are not used anymore, it could be interesting to keeps tracks of touchy commands in a cheatsheet before removing.

`_stack.md` could elvolve during project lifetime, one of its goals is to be usefull as much for devs, as for sysadmins. 
It contains keyword that can help you to find some *technologies* used in the past.

## /!\ Warning /!\

From the moment when you store sensitive data into these .md file you should be carefull.  
`_memo.md` **should never contains publicly exposed environments credentials and should not be publicly avalaible.** 

## License

[MIT](https://choosealicense.com/licenses/mit/)