# Git commit

Git commit komennolla tallennetaan repon muutokset.

## Kuvaus

Gitin commit -komennolla luodaan pysyvä muutos, johon tallennetaan indeksin sisältö ja commitin sisältöä kuvaava viesti.
Uusi committi on HEADin suora seuraaja, yleensä haaran kärki. Haara päivitetään aina osoittamaan uusimpaan committiin.

## Komennon käyttö ja valinnat

Commitoitava sisältö voidaan valita käyttämällä git "add" -komentoa. Toinen tapa jo työpuussa oleville tiedostoille on antaa commit -komentoon ensimmäisenä argumenttina 'a'.
Tällöin kaikki työpuussa olevien tiedostojen muutokset sisällytetään committiin.

Commiteille tulee aina antaa sen sisältöä kuvaava viesti. 
Näin on helppo katsoa, missä kohdin eri muutokset on tehty. Tästä on paljon apua, jos joudutaan palaamaan repon tai tiedoston aiempaan versioon.

Käyttämällä --interactive tai --patch switcheja voidaan yksittäin valita committiin sisällytettävät tiedostot ja tiedostojen muutokset. 

Tilanteessa, jossa huomaat virheen tekemässäsi commitissa, voit palauttaa edellisen version komennolla "git reset".


Alla komennon "git commit -h" tulostus.
```
usage: git commit [<options>] [--] <pathspec>...

    -q, --quiet           suppress summary after successful commit
    -v, --verbose         show diff in commit message template

Commit message options
    -F, --file <file>     read message from file
    --author <author>     override author for commit
    --date <date>         override date for commit
    -m, --message <message>
                          commit message
    -c, --reedit-message <commit>
                          reuse and edit message from specified commit
    -C, --reuse-message <commit>
                          reuse message from specified commit
    --fixup <commit>      use autosquash formatted message to fixup specified commit
    --squash <commit>     use autosquash formatted message to squash specified commit
    --reset-author        the commit is authored by me now (used with -C/-c/--amend)
    -s, --signoff         add Signed-off-by:
    -t, --template <file>
                          use specified template file
    -e, --edit            force edit of commit
    --cleanup <mode>      how to strip spaces and #comments from message
    --status              include status in commit message template
    -S, --gpg-sign[=<key-id>]
                          GPG sign commit

Commit contents options
    -a, --all             commit all changed files
    -i, --include         add specified files to index for commit
    --interactive         interactively add files
    -p, --patch           interactively add changes
    -o, --only            commit only specified files
    -n, --no-verify       bypass pre-commit and commit-msg hooks
    --dry-run             show what would be committed
    --short               show status concisely
    --branch              show branch information
    --ahead-behind        compute full ahead/behind values
    --porcelain           machine-readable output
    --long                show status in long format (default)
    -z, --null            terminate entries with NUL
    --amend               amend previous commit
    --no-post-rewrite     bypass post-rewrite hook
    -u, --untracked-files[=<mode>]
                          show untracked files, optional modes: all, normal, no. (Default: all)
    --pathspec-from-file <file>
                          read pathspec from file
    --pathspec-file-nul   with --pathspec-from-file, pathspec elements are separated with NUL character
```
