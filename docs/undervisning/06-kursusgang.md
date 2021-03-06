# 06 - Basic Cryptography

## Noter til dagens tekst

!!! note "Resumé af 'Basic Cryptography' (Bishop kap. 10)"
    Overordnet mål for kryptering er at hemmeligholde krypteret tekst (her også: data), men kan også bruges til at sikre integritet[^1].

    - **Symmetric cryptosystems**: Samme nøgle  til kryptering / dekryptering.   
      **Principper:**
        - **Transposition ciphers**: Flytter rundt på tegn i teksten; ændrer dem ikke.  
          - Eksempel: **rail fence cipher** (jf. pp. 291 + 292), som skriver teksten på to linjer og oppefra og ned i stedet for venstre mod højre.  
        - **Substitution ciphers**: Ændrer tegn i teksten; flytter dem ikke.   
          - Eksempler: **Vigenère Cipher** og **One time Pad**.
      - **Prominente eksempler på symmetric cryptosystems**:
        - **DES** (Data Encryption Standard): Udviklet af IBM i årene før 1974 under navnet LUCIFER, modificeret og adopteret som standard i 1976. Bruger *både* Transposition og Substitution. Anses som usikker siden 1998, i 2001 kommer AES og NIST pensionerer DES officielt i 2005. Trippel DES er den eneste implementering, af DES, der stadig anses for sikker (af NIST).
        - **AES** (Advanced Encryption Standard): Fra 2001, bruger Rijndael kryptosystemet. Succesfulde angreb er usandsynlige (men nok teoretisk mulige)[^2].

    - **Public Key Cryptography**: Krypterer med en nøgle dekrypterer med en anden.   
      **Principper:**   
        - **Private / public key**: Krypterer med offentlig nøgle; dekrypterer med privat nøgle (gør man det omvendt kan man verificere afsender ved at dekryptere med offentlig nøgle; eksempel herpå er digitale signaturer).   
        - **Kræver Key infrastructure**: Der skal findes en eller anden måde at udveksle nøgler på.
      - **Prominente eksempler på Public Key Cryptography:**
        - **El Gamal** og **RSA** (evt. implementeret med **Elliptic Curve Ciphers**).

    - **Cryptographic Checksums**: Envejsfunktion, der opfylder følgende (jf. def. 10-4 pp. 316):   
    1) For enhver tekst er checksummen nem at udregne.   
    2) For enhver checksum er det usandsynligt at finde den tilhørende tekst.   
    3) For enhver text er det usandsylligt at finde en anden tekst med samme checksum.      
      - Eksempler: **MD4** & **MD5**, **RIPEMD-160**, **HAVAL**, **Secure Hash Algorithm** (SHA-1, 224, 256, 384, 512).

    - **Digital Signatures**: En digital signatur er en konstruktion, der autentificerer afsender *og* indhold (nonrepudiation) til en ikke-indvolveret 3. part. (def. 10-7 pp. 318).
      - Digitale signaturer med symmetrisk kryptering, kræver betroet 3. part, som holder nøgler fra begge parter, der dekrypterer med afsenders nøgle (samme som har krypteret) krypterer på ny med modtagers nøgle og videresender. Herefter kan de to tekster i tvilvstilfælde sammenlignes og skal så være ens.
      - Digitale signaturer med asymmetrisk kryptering, signerer blot med private key og så kan alle verificere ved at dekryptere med public key.


## Noter fra undervisningen ([slides](https://github.com/kramse/security-courses/blob/master/courses/system-and-software/system-security/7-basic-cryptography.pdf))

Læs mere om kryptografi på [crypto-class.org](https://www.coursera.org/learn/crypto) <- matematik tungt.

- Ofte anvendes public/private key kryptografi til at kryptere en fælles "sessionsnøgle" (bredt forstået), som kan kommunikeres til hver enkelt modtager. På denne måde kan data krypteres een gang til mange modtagere og det er kun dem, der har modtaget en sessionsnøgle, der kan læse data.

- Kryptografiske principper (kramse-slide 21)


- AES gennemgang (med mindre fejl):

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/mlzxpkdXP58" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></center>

- RSA (Rivest-Shamir-Adleman): Opererer på store primtal. Nøglestørrelser 1.024 til 4.096 bits nøgler.

- [SHA-3](https://en.wikipedia.org/wiki/SHA-3) er den nyeste Secure Hashing Algorithm fra [NIST](https://en.wikipedia.org/wiki/National_Institute_of_Standards_and_Technology).

- Diffie-Hellman exchange - se kramse-slide nr 31 for DH exchange-figur med maling.

- [Elliptic Curve cryptography](https://en.wikipedia.org/wiki/Elliptic-curve_cryptography); nemt at regne den ene vej, svært at regne den anden vej.

- TLS: Undersøg evt. statistik for brug af forskellige versioner til slide til eksamen (hvad kører alexa top 100 f.eks.). Sårbar overfor "down grade attacks", hvis man ikke aktivt slår gamle versioner fra.

[^1]: En krypteret tekst, der er ændret i transit, vil typisk ikke (meningsfuldt) kunne dekrypteres.  
[^2]: Bishop pp. 305.
