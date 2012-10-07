Перенос untracked файлов в папку `~/.Trash` с сохранением относительных путей.

    git config --global alias.uz "ls-files --directory -z -o --exclude-per-directory=.gitignore"
    git uz | cpio -pdumv0 ~/.Trash

Однако, придётся и руками за собой почистить, не придумал, как удалить в одну строчку =(

    git uz | xargs -0 -I {} rm -rf {}