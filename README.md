# Bytesized Bash

Bytesized Bash (here) is an opinionated way to learn bash scripting. It's targeted toward computer professionals 
for the [rpm]() family of Linux distributions who uses the bash command line frequently but hasn't found the time
or inclination to start automating small tasks.

We'll focus on bash 5. It's available for all platforms, including Windows and OSX. OSX's default shell is [zsh](),
a generalization of bash. Many bash techniques carry over to zsh and are often even easier or more elegant. We'll
discuss those differences in more depth later.

## Format

The format is pretty simple: start at the beginning and work your way through each module (file) in the directory `src/module.d`. `src/module.d/README.md` will tell you the reading order. Bash's "read-eval-print loop" or repl lends itself to a certain style of learning first popularized with LISP and later scheme: 1) think about what a command will do, 2) issue the command and 3) test your hypothesis: did the command do what you expected? Think, do, test; rinse, repeat. You teach yourself in about the smallest increment possible, a single command or short sequence of commands. It may seem glacial at first and at times you might flail, but the teacher is always available because that teacher is you.

To start you'll just need your favorite text editor and bash. Working on your own machine (laptop, pc) 
will be helpful in some of the later modules, especially if you're missing some supporting tools like 
`sed`, `grep` and `awk`. But if you installed your Linux using any modern rpm-based distribution, you'll have all
you need.

## Start (and Layout)

1. Do you have the underlying commands you need?
   ```bash
   for _c in git curl bash sed awk grep; do type -p ${_c} && ${_c} --version || >&2 echo "${_c} not found"; done
   ```
   You need `bash` and either `git` or `curl`. 

2. Get the content (this stuff) using either `git` (preferred) or `curl`:
   ```bash
   git clone https://www.github.com/mcarifio/bytesized-bash || \
     { curl -Ss https://www.github.com/mcarifio/something | tar -xaf - }
   cd bytesized-bash
   tree .
   .
   ├── LICENSE
   ├── README.md
   └── src
       └── module.d
           ├── README.md
           └── why-bash.md
   ```

3. Open `src/module.d/README.md` in your editor. It will tell you other files to open.

4. In a terminal window running bash, think and issue commands.

5. Profit

   
   






