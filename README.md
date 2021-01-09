# phpcs-pre-commit-hook
A simple script to conform to phpcs standards before committing PHP code

A git pre-commit hook for running [PHP Code Sniffer](https://github.com/squizlabs/PHP_CodeSniffer) to ensure code conforms to PHP coding standards. It checks only PHP files before the code is committed.

Inspired by [Enforce code standards with composer, git hooks, and phpcs](http://tech.zumba.com/2014/04/14/control-code-quality/) and https://github.com/smgladkovskiy/phpcs-git-pre-commit and https://gist.github.com/BrizzleRocker/62ed61b37acf05344d4bce894e719251 . Installer checks OS on hosting machine and installs needed hooks for platform.

## Installation

Each git repository has a hooks directory inside the .git directory. Copy the pre-commit file and paste it in your directory and make the file executable using `chmod +x pre-commit`. If you have already using a pre-commit script then add this code in that file.

## Usage

Run `git commit` and the pre-commit hook will check the files like if you run
    
    php -l -d display_errors=0 /path/to/file.php 
    phpcs --colors /path/to/file.php
