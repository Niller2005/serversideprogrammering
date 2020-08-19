# Serversideprogrammering

> ## Beskriv hvordan kommunikationen foregår (HTTP requests) både statisk og dynamisk serverside [redigeret: Dynamisk som i et dynamisk site med PHP]

> ## Hvad er en HEAD request?
>
> Et HEAD request henter kun metadata, så det bliver brugt mest til at tjekke om en ressource eksistere eller er blevet opdateret, tjekke "request size" eller type.

> ## Hvad er en GET request?
>
> Et GET request henter metadata _og_ "content" fra en ressource. Så hvis du vil have data (typisk JSON eller XML) med i dit request skal du bruge GET.

> ## Hvilken bruger flest ressourcer?
>
> GET bruger flere ressourcer end HEAD, men det er kun det betyder ikke ret meget i dag, da båndbrede ikke et problem. Det du får mest performance ud af er at optimere dit RESTful API.

> ## Hvad er distribueret- , kontra monolitisk arkitektur?
>
> En monolistisk applikation, er en applikation der inderholder alt i et project (Frontend, Business logic, Databse access, og intergration med andre externe services)
>
> Fordele ved monolitisk arkitektur
>
> - Nem at deploye (Kan f.eks. bare uploade til en FTP)
> - Nem at teste
> - Nem at skalere horizontalt, ved at starte flere servere op og smide dem bag en loadbalancer
>
> Ulemper ved monolitisk arkitektur
>
> - Et projekt stiger hurtigt i størelse og kompleksitet
> - Kan hurtigt blive uoverskueligt og svært at sætte sig ind for ny folk
> - Du skal deploye hele applikationen hver gang hvilket kan give downtime
> - Besværligt at lave små og hurtige ændringer
> - Er låst ude fra nye teknologiere
>
> Idén med en distribueret arkitektur (Microservices) er at du splitter en monolistisk arkitektur op i mindre "services". Eksempel:
> ![Microservices](/assets/images/0_nQZhIgz34givPDhY.png)
>
> Fordele ved distribueret arkitektur
>
> - Hurtigt at udvikle nye på
> - Hurtigere at sætte sig en i en lille service for nye folk
> - Du kan opdatere en service ad gangen og komme tæt på "near-zero" downtime
> - Nemt at adoptere nye teknologier
> - Kan skalere hver service for sig selv
> - Nemt at automatisere skalering
> - Ikke låst til en kodebase, hvilket kan gøre det nemmere at finde folk
>
> Ulemper ved distribueret arkitektur
>
> - Flere ting at "holde styr på"
> - Øget kompleksitet iht. kommunikation mellem services
> - Øget kompleksitet iht. testing og deployment, det bliver næsten nød til at blive automatiseret
> - Mere besværligt at lave ændringer der involvere flere services.

> ## Beskriv med en model en microservice arkitektur og hvordan der kommunikeres. Eventuelt med dit eget eksempel.

> ## Beskriv en eller flere microservices og forklar hvordan man kan anvende den/dem. Det skal være med baggrund i enten din egen #softwareløsning eller i et tænkt eksempel [redigeret: Spørgsmål 7 indgår i spørgsmål 6. Spørgsmål 6, var tænkt som en model for arkitektur og spørgsmål 7 som en beskrivelse. Det beklager jeg meget].
