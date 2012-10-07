Перенос untracked файлов в папку `~/.Trash` с сохранением относительных путей.

    git ls-files --directory -o -z --exclude-per-directory=.gitignore | cpio -pdumv0 ~/.Trash

Однако, придётся и руками за собой почистить, не придумал, как удалить в одну строчку =(

    git ls-files --directory -o -z --exclude-per-directory=.gitignore | xargs -0 -I {} rm -rf {}