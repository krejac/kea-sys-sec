# 07 - Malware, Intrusion, Vulnerabilities

## Noter til dagens tekst

!!! note "Resumé af 'Malware' (kap. 23)"
    **Def. 23-1.** *Malicious logic*, more commonly called *malware*, is a set of instructions that cause a site's security policy to be violated.   
    **Def. 23-2.** A *Trojan horse* is a program with an overt (documented or known) purpose and a covert (undocumented or unexpected) purpose.   
    A **rootkit** is a pernicious Trojan horse. It hides itself on a system so it can carry out its actions without detection. (Kan være uhyggeligt svære at komme af med.)   
    **Def. 23-3.** A *propagating Trojan horse* (also called a *replicating Trojan horse*) is a Trojan horse that creates a copy of itself.   
    **Def. 23-4.** A *computer virus* is a program that inserts (a possibly transformed version of) itself into one or more files and then performs some (possibly null) action.   
      - Virusser opererer i to faser:   
        1. Insertion phase; hvor virussen indsætter sig selv i programkode.   
        2. Execution phase; hvor virussen udfører en handling.   
    **Def. 23-12.** A *Polymorphic* virus is a virus that changes the form of its decryption routine each time it inserts itself into another program.
    **Def. 23-14.** Worm
    **Def. 23-15.** Bot
    **Def. 23-17.** Logic bomb
    **Def. 23-18.** Adware
    **Def. 23-20.** Spyware
    **Def. 23-21.** Ransomware
    **Phishing** og **Spearphishing**

    **Theorem 23.2** It is undecidable whether an arbitrary program contains a malicious logic.

    **Defence**
    Behavioral signatures, static analysis, behavioral analysis    
    Sandboxing (containment)

!!! note "Resumé af 'Vulnerability Analysis' (kap. 24)"
    Ikke læst; noter fra undervisningen:   
    Blackbox, greybox, whitebox   
    Rules of engangement (kramse-slide 27).   
    [CVE - Common Vulnerabilities and Exposures](https://en.wikipedia.org/wiki/Common_Vulnerabilities_and_Exposures)
    [CWE - Common Weaknesses and Exposures](https://en.wikipedia.org/wiki/Common_Weakness_Enumeration)

*Find gerne tre spørgsmål til dages tekst, som skal søges besvaret i løbet af undervisningen. Det kan være eks. forståelsesmæssige spm. til anvendelighed af stoffet eller generel perspektivering.*

1. {Spørgsmål 1}
2. {Spørgsmål 2}
3. {Spørgsmål 3}

## Noter fra undervisningen ([slides](https://github.com/kramse/security-courses/blob/master/courses/system-and-software/system-security/7-malware-intrusion-vulnerabilities.pdf))

### Kapitel 23 - Malware

**Program integrity checker**   
- Advanced Intrusion Detection Environment ([AIDE](https://en.wikipedia.org/wiki/Advanced_Intrusion_Detection_Environment))

**Eksempler på Malware**   
- [Morris Worm](https://en.wikipedia.org/wiki/Morris_worm) (kramse-slide s. 10)   
- [Stuxnet](https://en.wikipedia.org/wiki/Stuxnet) (kramse-slide s. 11)   

![Morris worm disk](https://upload.wikimedia.org/wikipedia/commons/b/b6/Morris_Worm.jpg )

**Værktøjer**   
[Maltrail](https://github.com/stamparm/MalTrail) is a malicious traffic detection system.   
OWASP [Juice Shop](https://github.com/bkimminich/juice-shop): Probably the most modern and sophisticated insecure web application

### Kapitel 24 - Vulnerability Analysis

**Penetration testing**
[OWASP Penetration testing methodologies](https://www.owasp.org/index.php/Penetration_testing_methodologies)

Kig kramse-slides igennem.

**Buffers and stacks**
<center><iframe width="560" height="315" src="https://www.youtube.com/embed/1S0aBV-Waeo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

**Return oriented programming**
