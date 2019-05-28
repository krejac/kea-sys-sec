# 08 - Secure Systems Design and Implementation

## Noter til dagens tekst

!!! note "Resumé af 'Secure Design' (kap. 14)"
    *Gennemgang af ni principper for sikre systemer.*

    **Principle of Least Privilege** (def. 14-1):   
    Et subjekt skal kun have de privilegier, der er nødvendige for at gennemføre dets opgave.   
    **Principle of Least Authority** (def. 14-2): <- *Bør ikke uddybes til eksamen, da forskellen til den forrige er akademisk.*  
    Et subjekt skal kun have den autoritet, der er nødvendig for at gennemføre dets opgave.   
    **Principle of Fail-Safe Defaults** (def. 14-3):    
    Medmindre et subjekt er givet *eksplicit* adgang til et objekt, skal det formenes adgang til objektet.   
    **Principle of Economy of Mechanism** (def. 14-4):   
    Sikkerhedsmekanismer skal være så simple som muligt.   
    **Principle of Complete Mediation** (def. 14-5):   
    *Al* adgang til objekter skal tjekkes for at sikre subjektet har lov til at tilgå det.   
    **Principle of Open Design** (def. 14-6):   
    Sikkerheden i sikkerhedsmekanismerne, må aldrig hvile på hemmeligholdelse af disse (et eksempel som forbryder sig mod dette princip er bagdøre til kryptering).   
    **Principle of Seperation of Privilege** (def. 14-7):   
    Der må ikke tildeles adgang (til et objekt i systemet) baseret på en enkelt betingelse.   
    **Principle of Least Common Mechanism** (def. 14-8):   
    Mekanismer til brug af systemet, må ikke deles bør ikke deles med andre (eks. flere systemer på samme maskine).  
    **Principle of Least Astonishment** (def. 14-9):   
    Brugere skal forstå *hvordan* en sikkerhedsmekanisme forbedrer sikkerheden *og* være simpel.   

!!! note "Resumé af 'Representing Identity' (kap. 15)"
    *Identiteter er basis for al adgangskontrol (access control mechanisms)*

    **What Is Identity**   
    En identitet repræsenterer en *unik enhed*.   
    **Files and Objects**   
    Lokale systemer identificerer objekter ved navn. Distribuerede systemer (f.eks. internettet) identificerer objeker ved navn *indeholdene* placering (f.eks. en url, som består af protokol, server, navn).   
    **Users**   
    En bruger er en identitet bundet op på en specifik *unik enhed* (f.eks. en person eller gruppe). En unik enhed kan have flere brugere (eks. til forskellige brugssituationer).   
    **Groups and Roles**   
    En *unik enhed* kan være sammensat af flere *unikke enheder* (eks. en gruppe af brugere). Medlemmer i en *unik enhed* skal kunne skelnes fra hinanden.   
    **Naming and Certificates**    
    Certifikater binder kryptografiske nøgler til *unikke enheder*.     
    **Identity on the Web**    
    [UDFYLDES TIL UNDERVISNING]     
    **Anonymity on the Web**   
    [UDFYLDES TIL UNDERVISNING]    
    **DNSSEC**
    Sikrer integritet; validerbar helt op til roden af dns.

    Forståelse for hvordan en *identitet* er bundet til den *unikke enhed* giver indsigt i troværdigheden af den pågældende *unikke enhed*.


!!! note "Resumé af 'Access Control Mechanisms' (kap. 16)"
    Adgangskontrolmekanismer (access control mechanisms) implementerer kontrol på subjekter og objekter i systemer. Typisk er det ejeren af data, der definerer hvem der må få adgang til data. (*Access Control Lists*, *Capability Lists*, *Lock and Keys*.)

    Med nogle adgangskontrolmekanismer (*ring-based*, eks. cpu'er) er det systemet, der definerer hvem der har adgang til hvad. I disse tilfælde skal reglerne dog være meget velovervejede.

    *Propagated Access Control Lists*?

### Artikler
- [Setuid Demystified](https://people.eecs.berkeley.edu/~daw/papers/setuid-usenix02.pdf) (Se evt. nedenstående om setuid, setgid og sticky bits.)
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/rXZJLqbZ03Y" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>   

- [Some thoughts on security after ten years of qmail 1.0](http://cr.yp.to/qmail/qmailsec-20071101.pdf)   
**How to keep software safe:**   
Answer 1: *eliminating bugs − > Enforcing explicit data flow, Simplifying integer semantics, Avoiding parsing.*   
Answer 2: *eliminating code − > Identifying common functions, Reusing network tools, Reusing access controls, Reusing the filesystem.*   
Answer 3: *eliminating trusted code − > Accurately measuring the TCB, Isolating single-source transformations, Delaying multiple-source merges, Do we really need a small TCB?*   

- [Wedge: Splitting Applications into Reduced-Privilege Compartments](http://css.csail.mit.edu/6.858/2014/readings/wedge.pdf)   
Wedge 

*Find gerne tre spørgsmål til dages tekst, som skal søges besvaret i løbet af undervisningen. Det kan være eks. forståelsesmæssige spm. til anvendelighed af stoffet eller generel perspektivering.*

1. {Spørgsmål 1}
2. {Spørgsmål 2}
3. {Spørgsmål 3}

## Noter fra undervisningen ([slides](https://github.com/kramse/security-courses/blob/master/courses/system-and-software/system-security/8-secure-systems-design.pdf))

Dette er en test for at se hvordan det er at skrive her[^1].

!!! Note
    Husk at man kan lave en blok med en note midt i det hele. Det er sådan set ret blæret. Man skal bare huske syntaksen. Men sådan er det jo at skrive i markdown.

[^1]: Man kan også bruge fodnoter.  
