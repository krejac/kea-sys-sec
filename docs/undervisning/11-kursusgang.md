# 11 - Forensics 2: Incident Response

## Noter til dagens tekst

!!! note "Resumé af 'Attacks and Responses' (kap. 27)"
    ### Begreber:
    > *Security Policies* define what is, and what is not, allowed.   

    **Def. 27-1:** An *attack* is a sequence of actions that create a violation of a security policy.   
    **Def. 27-2:** A *goal* is what an attacker hopes to achieve.  
    **Def. 27-3:** A *target* of an attack is the entity that the attacker whishes to affeck.   
    **Def. 27-4:** A *multistage attack* is an attack that requires several steps to achieve its goal.

    ### Intrusion Response
    **Incident prevention**:   
    - Ideelt set bliver indbrudsforsøg stoppet *inden* de gennemføres.   
    - *Diversitet* er en metode for at forhindre indbrud, da en sårbarhed i ét system typisk ikke også vil eksistere på et andet (eksempeler er *moving target defence* (pp. 973), [ASLR](https://en.wikipedia.org/wiki/Address_space_layout_randomization) eller [KARL](https://www.theregister.co.uk/2017/06/19/thats_random_openbsd_adds_more_kernel_security/))  

    **Def 27-5:** An *attack surface* is the set of entry points and data that the attackers can use to compromise a system.     

    **Defenders Dilemma:** En angriber skal kun finde én sårbarhed; en forsvarer skal lukke alle.   
    **Attackers Dilemma:** En angriber skal hele tiden undgå at blive set; en forsvarer skal bare spotte ham én gang (*eget bud på den omvendte problemstilling*).   

    ### Intrusion Handling
    **Def. 27-8:** A computer security incident response team (CSIRT) is a team established to assist and coordinate responses to a security incident among a defined constituency.   

    *Overlapper med Incident Handler's Handbook* (principperne går tilbage fra '89)    

    **Faser**   
    1) Preparation (forberedelse)   
    2) Identification (opdagelse)   
    3) Containment (inddæmning)   
    4) Eradication (udryddelse)   
    5) Recovery (genetablering)   
    6) Follow-up / Lessons Learned[^1] (opfølgning)   

## Noter fra undervisningen ([slides](https://github.com/kramse/security-courses/blob/master/courses/system-and-software/system-security/11-forensics-incident-response.pdf))

- Most attacks are multistage (and includes lateral movement).
- Example goals: access to systems for learning, stealing, for spamming, for embarrassment, political influence etc.
- Attack tree: en kæde af hændelser, der skal til for t opnå målet. Et træ har mange kombinationer, kæden er en sti igennem træet.

![](https://www.schneier.com/images/paper-attacktrees-fig1.gif)

- Real-time intrusion detection systems (IDS/IPS). Kig på trafik. Svært at opdage, da det er almindeligt at overføre store mængder data.
- Minimér *attack surface* ved at fjerne ikke-essentielle webrettede services.

**Pentesting**   
- Verification of the system in place   
- Examines procedural and operational controls   
- Is the system in fact installed and operated as expected    
- Example, is the firewall even enabled?   
- Penetration testing methodologies ([OWASP](https://www.owasp.org/index.php/Penetration_testing_methodologies))   

**Coordinating Response**   
- CERT/CSIRT (eks. DK-CERT, de nye sektor CERTs).   
- Standard document about Incident Response: [Expectations for Computer Security Incident Response](https://www.ietf.org/rfc/rfc2350.txt)   

**Digital Forensics / Computer Forensics**
- Kramses favorit def. af DF / CF (forskellig fra den i bogen):

> Computer Forensics involves the preservation, identification, extraction, documentation and interpretation of computer data.

*- Computer Forensics: Incident Response Essentials*

**Honeypots** - check [honeynet.org](http://honeynet.org/)

[^1]: "Incident Handler's Handbook" kalder denne fase *Lessons Learned*.  
