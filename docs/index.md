# STARTSIDE

## Intro

Disse sider er skrevet af Kresten til Kresten i forbindelse med kurset Systemsikkerhed på KEA ([arkiv](https://web.archive.org/web/20190318201143/https://kompetence.kea.dk/kurser-fag/systemsikkerhed)) foråret 2019. Den anvendte litteratur er "Computer Security - Art and Science" af Matt Bishop ([Amazon](https://www.amazon.co.uk/Computer-Security-Science-Matt-Bishop/dp/0321712331/)).

Siderne er sat op med MkDocs; nedenstående er en ultra kort vejledning til hertil.

## MkDocs local docs

For full documentation visit [mkdocs.org](http://mkdocs.org).

### Hurtig installation på Ubuntu 18.10

Installér MkDocs og pip med apt, derefter temaet [material](https://squidfunk.github.io/mkdocs-material/) med pip.
    
```bash
$ sudo apt install mkdocs && python3-pip
$ pip3 install mkdocs-material
```

### Kommandoer

* `mkdocs new [dir-name]` - Opret nyt projekt.
* `mkdocs serve` - Start selv-opdaterende dokumentationsserver.
* `mkdocs build` - Byg dokumentations sitet.
* `mkdocs help` - Print denne hjælp (på engelsk).

### Projektlayout

    mkdocs.yml    # Konfigurationsfil.
    docs/
        index.md  # Dokumentationssitets hjemmeside
        ...       # Andre markdownsider, billeder og andre filer
	/undervisning/ 
	    01-kursusgang.md  # Noter til 1. kursusgang
	    02-kursusgang.md  # Noter til 2. kursusgang
	    ...
	/eksamen 
	    ...  # Der dukker nok noget op her
