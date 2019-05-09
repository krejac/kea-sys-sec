# 05 - Hybrid Policies / Breaking out

## Noter til dagens tekst

!!! note "Resumé af 'Hybrid Policies' (kap. 8)"
    En del organisationer har brug for alternative politikker, som kombinerer een eller flere af CIA-politikkerne på forskellig vis.Eksempler herpå er:

    - *[Chinese Wall Model](https://en.wikipedia.org/wiki/Chinese_wall#Computer_science)*: Skal forhindre interessekonflikt ved ikke tillade et subjekt at tilgå **både** A og B, men gerne enten A eller B (sikrer confidentiality & integrity)(se def. 8-1, 8-2 og 8-3).
    - *Clinical Information Systems Security Policy*: Skal sikre fortrolighed og integritet OG autorisere den der laver ændringer (se def. 8-6, 8-7 og 8-8).   
    - *Originator Controlled Access Control*: Skal sikre at ophavsrettigheder bliver overholdt. Eksempel: Digital Rights Management (DRM).   
    - *[Role-Based Access Control](https://en.wikipedia.org/wiki/Role-based_access_control)*: Adgang baseret på jobfunktion (rolle) (eks. et AD som har en række roller).   
    - *Break-the-Glass policies*: Skal kunne tilsidesætte almindelige adgangsstyring i situationer hvor behovet opstår. Eks. skadestue hvor patient er bevidstløs og samtykke ikke kan indhentes.
    - *Covert Channels / Side Channels and Deducibility*: Se dagens slides slide nr. 17-2X.

Derudover skulle der også læses op på 'row hammer', som går ud på at flippe bits uden at tilgå dem i moderne ram, hvor de enkelte bits aflader ind i naborækkerne.

*Find gerne tre spørgsmål til dages tekst, som skal søges besvaret i løbet af undervisningen. Det kan være eks. forståelsesmæssige spm. til anvendelighed af stoffet eller generel perspektivering.*

1. {Spørgsmål 1}
2. {Spørgsmål 2}
3. {Spørgsmål 3}

## Noter fra undervisningen ([slides](https://github.com/kramse/security-courses/blob/master/courses/system-and-software/system-security/5-hybrid-policies.pdf))

Lav tidslinje over Row Hammer's udvikling fra initiel paper over teoretiske exploits til javascript og til sidst NET HAMMER (netværks angreb med Row Hammer) og DRAMMER (Android rooting med Row Hammer).

[Flipping Bits in Memory Without Accessing Them:
An Experimental Study of DRAM Disturbance Errors](../assets/kim-isca14-flipping-bits.pdf)    
På mange moderne hukommelsesmoduler er det muligt at flippe bits i nærliggende

2015 - Google Project Zero: [Exploiting the DRAM rowhammer bug to gain kernel privileges](https://googleprojectzero.blogspot.com/2015/03/exploiting-dram-rowhammer-bug-to-gain.html)

![Rapid row activations (yellow rows) may change the values of bits stored in victim row (purple row).](https://upload.wikimedia.org/wikipedia/commons/c/c8/Row_hammer.svg)

[^1]: Man kan også bruge fodnoter.  
