# 01 - Overview of Computer Security

## Noter til dagens tekst

!!! note "Resumé af 'An Overview of Computer Security' (kap. 1)"
    IT-sikkerhed afhænger i høj grad af organisatorisk tillid ('trust'). Tillid er grundlaget for sikkerheden, som opbygges i et system. Hvis tilliden er velfunderet kan ethvert system gøres sikkert (nok). Er tilliden derimod malplaceret, kan et system ikke gøres sikkert på nogen måde.
    Dermed bliver sikkerhed også et relativt begreb, da en angriber med nok ressourcer næsten altid vil kunne bryde sikkerhedsmekanismer og procedurer (den velfunderede tillid). Målet er at gøre det dyrere for angriberne at angribe end at opnå målet på anden vis.


### Begreber
**C-I-A**: *Confidentiality* (fortrolighed), *Integrity* (troværdighed / integritet), *Availability* (tilgængelighed).   
**Trussel** (threat): Et *potentielt* sikkerhedsbrud.   
**Aflytning** (snooping): [Selvindlysende]   
**Modifikation** (modification): Eks. ved man-in-the-middle.   
**Maskering** (spoofing): Udgive sig for at være en anden.    
**Benægtelse af afsendelse** (repudiation of origin): "Det har jeg aldrig sendt" / "Det har jeg aldrig bestilt / bedt om".   
**Benægtelse af modtagelse** (denial of reciept): "Det har jeg aldrig modtaget."   
**Forsinkelse** (delay): [Selvindlysende]   
**Afskær service** (denial of service): [Selvindlysende]   

!!! note "Resumé af 'Access Control Matrix' (kap. 2)"
    Access Control Matrix'en er det primære abtraktionsniveau i IT-sikkerhed (eks.: adgangsrettigheder i unix; read, write, execute).

## Noter fra undervisningen ([slides](https://github.com/kramse/security-courses/blob/master/courses/system-and-software/system-security/1-overview-computer-security.pdf))

### Kramses guldkorn
- Man skal have "passende paranoia".
- God sikkerhed er lille investering, højt afkast. Dårlig sikkerhed omvent.

- Goals of Security:
    - Prevention - means that an attack will fail
    - Detection - determine if attack is underway, or has occured - report it
    - Recovery - stop attack, assess damage, repair damage

!!! note  "Definition 20-6."
    A _trusted computing base_ (TCB) consists of all protection mechanisms within a computer system – including hardware, firmware, and software – that are responsible for enforcing a security policy
