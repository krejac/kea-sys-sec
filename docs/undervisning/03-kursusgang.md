# 03 - Security Policies / Confidentiality Policies

## Noter til dagens tekst

!!! note "Resumé af 'Security Policies' (Bishop kap. 4)"
    - Sikkerhedspolitikker kan enten være antydet ved en fælles forståelse i organisationen eller uformelle politikker defineret ved en fælles tolkning i organisationen.    
    - *Tillid* er basis for alle politikker og håndhævelsesmekanismer. Man *antager* at politikker og principper overholdes og man gør antagelser om at software og hardware fungere sikkert (efter forskrifterne).    
    - Ved at forstå de underliggende antagelser og tilliden involveret i et system øges forståelsen af sikkerheden i systemet.    

!!! note "Resumé af 'Confidentiality Policies' (Bishop kap. 5)"
    Bell-LaPadula modellen gennemsyrer alle fortrolighedspolitikker. Bell-LaPadula modellen siger kort "[Read down; no read up. Write up; no write down](../assets/docs/Bell-LaPadula-figure.png)". Dette pricip, skulle gerne sikre at folk (eller processer) med lavere godkendelsesniveau ikke opnår indsigt i informationer på et højere godkendelsesniveau.   

    Andre teoretikere (eks. McLean[^1] [pp. 164]) har sået tvivl om aspekter i Bell-LaPadula modellen, men uanset hvad er den stadig grundlaget for størstedelen af alle fortrolighedspolitikker. Tvivlen har blot givet anledning til at man har opdaget kompleksiteten ved virkelige systemer (i modsætning til teoretiske).

### Bell-LaPadula explained

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/U_BMvYTfnuU" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

### Yderligere ressourcer

- Eksempler i Bishop Appendix G.
- [Campus Network Security: High Level Overview](https://nsrc.org/workshops/2018/myren-nsrc-cndo/networking/cndo/en/presentations/Campus_Security_Overview.pdf) [[lokal kopi](../assets/docs/Campus_Security_Overview.pdf)]
- [Campus Operations Best Current Practice](https://nsrc.org/workshops/2018/tenet-nsrc-cndo/networking/cndo/en/presentations/Campus_Operations_BCP.pdf) [[lokal kopi](../assets/docs/Campus_Operations_BCP.pdf)]
- [Mutually Agreed Norms for Routing Security (MANRS)](https://www.manrs.org/wp-content/uploads/2018/09/MANRS_PDF_Sep2016.pdf) [[lokal kopi](../assets/docs/MANRS_PDF_Sep2016.pdf)]


## Noter fra undervisningen ([slides](https://github.com/kramse/security-courses/blob/master/courses/system-and-software/system-security/3-security-policies.pdf))

Skal have styr på (til eksamen):

- DAC: [Discretionary Access Control](https://en.wikipedia.org/wiki/Discretionary_access_control) - Def. 4-13 (Læs også Wikipedia)
- MAC: [Mandatory Access Control](https://en.wikipedia.org/wiki/Mandatory_access_control) - Def. 4-14 (Læs også Wikipedia)
- RBAC: [Role-based Access Control](https://en.wikipedia.org/wiki/Role-based_access_control) - ikke i bog (Læs Wikipedia)

Policies:

- AUP: Acceptable Use Policies. Hvad må man / må man ikke på netværket.

- [MANRS](https://www.manrs.org/): *Mutual Acceptable Norms for Routing Security* - Manerer for acceptabel opførsel for internetoperatører.



[^1]: McLean siger at "givet nogle usikre antagelser kan man med Bell-LaPadulas Theorem bevise et usikkert systems er sikkert" [parafrasering]. Igen, det hele handler om man kan stole på sine antagelser.  
