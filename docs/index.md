# Forside

Disse sider er skrevet af Kresten til Kresten i forbindelse med kurset [Systemsikkerhed på KEA](https://kompetence.kea.dk/kurser-fag/systemsikkerhed) ([pdf](./assets/docs/KEA-brochure.pdf)) foråret 2019. Den anvendte litteratur er "[Computer Security - Art and Science](http://nob.cs.ucdavis.edu/book/book-aands2/index.html)"[^1] af Matt Bishop ([Amazon](https://www.amazon.co.uk/Computer-Security-Science-Matt-Bishop/dp/0321712331/)) og [Linux Basics for Hackers](https://www.hackers-arise.com/linux-fundamentals) af OccupyTheWeb ([Amazon](https://www.amazon.de/gp/product/1593278551/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&psc=1)).

Løbende opdateret lektionsplan kan findes på Zencurity's [GitBook-side](https://zencurity.gitbook.io/kea-it-sikkerhed/systemsikkerhed/lektionsplan).

Mine noter findes i menuen under punktet "Undervisning".

--------------------------------------------------------------------------------

Siderne er sat op med MkDocs; nedenstående er en ultra kort vejledning til hertil.

## MkDocs local docs

For full documentation visit [mkdocs.org](http://mkdocs.org).

### Hurtig installation på Ubuntu 19.04 (og 18.10)

Installér MkDocs og pip med apt, derefter temaet [material](https://squidfunk.github.io/mkdocs-material/) med pip.

```bash
$ sudo apt install mkdocs python3-pip
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

[^1]: [Matt Bishops egne slides til undervisning](http://nob.cs.ucdavis.edu/book/book-intro/slides/index.html)
