# 04 - Integrity and Availability Policies

## Noter til dagens tekst

!!! note "Resumé af 'Integrity Policies' (Bishop kap. 6)"
    Integritets politikker skal addressere problematikker med at sikre dataintegritet i "vildt varierede"[^1] miljøer. De er vigtige, da det i mange typer af organisationer er mere kritisk om data er til at stole på end om de eks. bliver holdt fortrolige.

    Intgritet kan forsøges bevaret ved at overholde nogle principper for drift[^2]

    - *[Adskildelse af ansvar](https://en.wikipedia.org/wiki/Separation_of_duties)*: Flere øjne på, hvis det er muligt.  
    - *Adskildelse af funktion*: Udviklere, udvikler ikke i produktion og kan ikke selv deploye til produktion.
    - *Auditering (revision)*: Analyse af systemer med det formål at undersøge hvad der sker hvornår samt hvem der har gjort hvad.

    Modeller: *[Biba](https://en.wikipedia.org/wiki/Biba_Model)*, *Lipner* (læs bog, ikke internet; der er forskel) og *[Clark-Wilson](https://en.wikipedia.org/wiki/Clark%E2%80%93Wilson_model)*. Se også Matt Bishops egne [undervisningsslides](http://nob.cs.ucdavis.edu/book/book-intro/slides/06.pdf).

    *Trust model*: Hvor integritets modeller behandler problematikken om at bevare et systems integritet, handler "trust" om tilliden til systemets initielle. Minder meget om formel epistemologi.   
    Tillid til entiteter både direkte og indirekte (transitiv / konditionel transitiv).

!!! note "Resumé af 'Availability Policies' (Bishop kap. 7)"
    Skal forhindre forskellige typer af Denial of Service. Eks. deadlock[^3] eller (D)DoS angreb[^4].

    Modellerne for beskrivelse af Availability Policies, Eks. Yu-Gligor (pp. 204 ->) og Millen (pp. 210 ->), har typisk to overornede politikker:

    - *User agrement*: Begrænsning på brug af ressourcer (eks. ingen flooding).
    - *Waiting Time*: Hvor lang tid man skal vente før der er tale om Denial of Service.

    SYN-flood er eksempel på DoS angreb og Cisco har implemeteret mitigering i noget af deres udstyr, som afventer fuldt TCP handshake før forbindelse overgives til udførende system for at undgå at ressourcer på sytemet bliver bundet op på ventende forbindelser.

Yderligere læsning: [TCP Synfloods
an old yet current problem](http://quigon.bsws.de/papers/2017/bsdcan/)

*Find gerne tre spørgsmål til dages tekst, som skal søges besvaret i løbet af undervisningen. Det kan være eks. forståelsesmæssige spm. til anvendelighed af stoffet eller generel perspektivering.*

1. Uddybning af User Agrement?
2. Generelt: hvilket niveau skal politikkerne implementeres på? (msk vs. tech)
3. {Spørgsmål 3}

## Noter fra undervisningen ([slides](https://github.com/kramse/security-courses/blob/master/courses/system-and-software/system-security/4-integrity-availability-policies.pdf))

- Jo mere der kan automatiseres af de her processer, desto bedre. I så fald bliver fejlene nemlig systematiske og kan programatikse rettelser kan føre systemet tilbage til et sikkert stade.

### [Relational Database](https://en.wikipedia.org/wiki/Relational_database) Management Systems ([RDBMS](https://en.wikipedia.org/wiki/Relational_database#RDBMS))

![RDBMS structure](https://upload.wikimedia.org/wikipedia/commons/5/57/RDBMS_structure.png)

Til forklaring af deadlocks brug [Dining Philosophers Problem](https://en.wikipedia.org/wiki/Dining_philosophers_problem). Forklar evt. også om [deadlock detection](https://en.wikipedia.org/wiki/Deadlock#Detection) (se også [Thrashing](https://en.wikipedia.org/wiki/Thrashing_(computer_science)) for sammenlignelig problemstilling på OS-niveau). 

[^1]: Ref. "environments vary wildly", "Summary" pp. 196.  
[^2]: Ref. "principles of operation", "Goals" pp. 173.
[^3]: En proces hindres adgang til ressource.
[^4]: Eks. SYN-flood (syn -> syn/ack -> ack).
