# leetcode repo template

Welcome to this repo! This is a template repo for storing your Leetcode solutions that can also take your solution files and automatically sort them into a navigatable markdown wiki. For more details, see [this repository](https://github.com/Zanger67/Leetcode-Progress-Tracker).

Instructions can be found below and also in [instructions.md](<instructions.md>) when this README gets overwritten. Feel free to delete it if you wish.


## Commands
By default, this will generate markdowns for each question you have a solution for only when it's newly created or there's been a change (to avoid redundant processes). If you want to reprocess the entire set of markdown files, add the `-r` flag to the python call.

```powershell
python .readme_updater/main.py -r
```

## General Important Information
Make sure to modify the `.env` file. Edit the one in this main folder called `.env.template` then change its name to `.env`.

**If you are using this template, the only thing you need to change is `LEETCODE_USERNAME` it will still work if you don't.**

You should be naming your files either in the form of `{difficulty}{number}...anything.{language}` or simply starting with the question number. If this format isn't followed, it will take the first number and use that. Some examples:
- `h1234.py`
- `m321.sql`
- `e987 something version 1 comments removed file.java`
- `15.c`


### Option 1 - Fork

1. Fork this repo.
2. Navigate to where you want to keep your Leetcode files on your computer.
3. Clone the repo (***make sure to have the `--recursive` tag in order to bring in the submodule as well***):

```powershell
git clone --recursive https://github.com/USERNAME/YOUR_REPO.git
```

4. Modify the values in the `.env.sample` file according to your needs and rename it to `.env`.

*Note: the checker will prioritize the .env that's present in the main directory over the Leetcode-Progress-Tracker directory.*

1. Place your solutions in the `my-submissions` folder.

All set! To generate a markdown, either run either `main.py` or `main.ipynb`.

```powershell
python .readme_updater/main.py
```

### Option 2 - Submodule

As long as you adjust `.env` accordingly, there should be no issue. `main.py` uses relative pathing to export the markdown files.

You can import the `.readme_updater` repo as a submodule into your own location if you wish.

1. Navigate to your Leetcode file directory.
2. Use the following command:

```powershell
git submodule add https://github.com/Zanger67/Leetcode-Progress-Tracker.git .readme_updater
```

`.readme_updater` at the end can be replaced with whatever directory name you wish to host the scripts.

3. Configure the `.env.sample` found inside the submodule folder (`.readme_updater` folder)

All set! To generate a markdown, either run either `main.py` or `main.ipynb`.

```powershell
python .readme_updater/main.py
```