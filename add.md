# Git add

Git "add" -komennolla lisätään tiedostoja indeksiin commitoitavaksi.

## Kuvaus 
Git "add" -komento päivittää indeksiin työpuusta löytyviä tiedostoja.
Optioiden avulla indeksiin lisättäviä tiedostoja voidaan valita tai poistaa polut tiedostoihin, jotka eivät enään ole työpuussa.

"Indeksi" sisältää snapshotin valituista työpuun tiedostoista. Tämän indeksin sisältö tulee olemaan seuraavan commitin sisältö. 
Tämän takia komento "git add" on ajettava aina ennen committia, jotta uusimmat muutoksen sisältyvät seuraavaan committiin.

## Komennon käyttö ja valinnat:
Alla komennon "git add -h" tulostus.
```
git add [<options>] [--] <pathspec>...

    -n, --dry-run         dry run
    -v, --verbose         be verbose

    -i, --interactive     interactive picking
    -p, --patch           select hunks interactively
    -e, --edit            edit current diff and apply
    -f, --force           allow adding otherwise ignored files
    -u, --update          update tracked files
    --renormalize         renormalize EOL of tracked files (implies -u)
    -N, --intent-to-add   record only the fact that the path will be added later
    -A, --all             add changes from all tracked and untracked files
    --ignore-removal      ignore paths removed in the working tree (same as --no-all)
    --refresh             don't add, only refresh the index
    --ignore-errors       just skip files which cannot be added because of errors
    --ignore-missing      check if - even missing - files are ignored in dry run
    --chmod (+|-)x        override the executable bit of the listed files
    --pathspec-from-file <file>
                          read pathspec from file
    --pathspec-file-nul   with --pathspec-from-file, pathspec elements are separated with NUL character
```
