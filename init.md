# Git init

Git init -komennolla luodaan uusi tyhjä Git repo tai alustetaan olemassa oleva.

## Kuvaus

Tämä komento luo tyhjän Git repon. Käytännösse se luo .git -hakemiston alihakemistoineen ja mallitiedostoineen. Se luo myös alustavan haaran ilman committeja.

`$GIT_DIR` ympäristömuuttujan avulla voidaan asettaa käytettäväksi jonkin muun tiedostopolun, kuin .git/. 

Komento voidaan myös ajaa olemassa olevassa hakemistossa. Se ei muuta sen sisältämiä tiedostoja ollenkaan.
Git init komento voidaan myös ajaa hakemistossa uudelleen sen siirtämiseksi johonkin toiseen hakemistoon (´--separate-git-dir` argumentilla) tai uusien mallitiedostojen saamiseksi. 

## Komennon käyttö ja valinnat

Alla komennon "git init -h" tulostus.
```
usage: git init [-q | --quiet] [--bare] [--template=<template-directory>] [--shared[=<permissions>]] [<directory>]

    --template <template-directory>
                          directory from which templates will be used
    --bare                create a bare repository
    --shared[=<permissions>]
                          specify that the git repository is to be shared amongst several users
    -q, --quiet           be quiet
    --separate-git-dir <gitdir>
                          separate git dir from working tree
```
