# Git push

Git push komennolla päivitetään paikallisen repositoryn sisältö etärepoon.

## Kuvaus

Komento päivittää etärepon viittaukset ajantasalle paikallisen repon viitausten kanssa ja lähettää tarvittavat tiedostot viitteiden päivittämiseksi.

Lisäämällä koukkuja voidaan saada mielenkiintoisia asioita tapahtumaan.

## Komennon käyttö ja valinnat

Kun push:in kohdetta ei määritellä komennon "repository" argumentissa, muutokset työnnetään `branch.*.remote` tiedostossa määriteltyyn sijaintiin.
Määrittelyn poissaollessa työnnetään muutokset oletuksena originiin.

Ellei toisin määritellä, komento push työntää muutokset tiedoston `push.default` mukaan. Työnnettävät muutokset voidaan määritellä `<refspec>` tai esim. --all, --mirror tai --tags optioilla.

Kun komennolle ei anneta ylimääräisiä argumentteja, työnnetään kaikki muutokset oletuksena annettuun ylätasoon.

```
usage: git push [<options>] [<repository> [<refspec>...]]

    -v, --verbose         be more verbose
    -q, --quiet           be more quiet
    --repo <repository>   repository
    --all                 push all refs
    --mirror              mirror all refs
    -d, --delete          delete refs
    --tags                push tags (can't be used with --all or --mirror)
    -n, --dry-run         dry run
    --porcelain           machine-readable output
    -f, --force           force updates
    --force-with-lease[=<refname>:<expect>]
                          require old value of ref to be at this value
    --recurse-submodules[=(check|on-demand|no)]
                          control recursive pushing of submodules
    --thin                use thin pack
    --receive-pack <receive-pack>
                          receive pack program
    --exec <receive-pack>
                          receive pack program
    -u, --set-upstream    set upstream for git pull/status
    --progress            force progress reporting
    --prune               prune locally removed refs
    --no-verify           bypass pre-push hook
    --follow-tags         push missing but relevant tags
    --signed[=(yes|no|if-asked)]
                          GPG sign the push
    --atomic              request atomic transaction on remote side
    -o, --push-option <server-specific>
                          option to transmit
    -4, --ipv4            use IPv4 addresses only
    -6, --ipv6            use IPv6 addresses only
```
