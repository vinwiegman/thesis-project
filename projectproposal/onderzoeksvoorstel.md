# Literature review
De analyse van juridische citatienetwerken is een groeiend onderzoeksgebied binnen de computational legal studies en de netwerkwetenschap. In deze benadering worden rechterlijke uitspraken gemodelleerd als knopen (nodes) en citaties tussen uitspraken als gerichte verbindingen (edges). Dit maakt het mogelijk om juridische systemen te analyseren als complexe netwerken, waarin structuur en relaties centraal staan.

Juridische citaten vormen al lang tijd de kern van juridisch onderzoek. Zoals aangetoond door Marx (1970), maken juristen gebruik van citaties om eerdere uitspraken te vinden en te volgen, waarbij uitspraken met elkaar verbonden worden in een netwerk van precedenten. Dit proces, ook wel “shepardization” genoemd, impliceert dat citaties betekenisvolle relaties presenteren tussen zaken. Het citatienetwerk kan daarmee worden opgevat als een weerspiegeling van de interne structuur van het recht.

Met de opkomst van computationele methoden is het mogelijk geworden om juridische citatienetwerken op grote schaal te analyseren. Een belangrijke studie in deze ontwikkeling is die van Fowler et al. (2007), die het volledige citatienetwerk van uitspraken van het Amerikaanse Supreme Court analyseren en een methode introduceren om de juridische relevantie van uitspraken te meten op basis van citatiepatronen. Hierbij ontwikkelen zij zogenoemde 'importance scores', die gebruik maken van zowel het aantal citaties dat een uitspraak ontvangt als de positie van deze uitspraak binnen het volledige netwerk. Door niet alleen het aantal citaties te tellen, maar ook rekening te houden met de structuur van het netwerk, ontstaat er een meer genuanceerde maat voor juridische relevantie. Door deze benadering wordt niet alleen gekeken naar hoe vaak een uitspraak wordt geciteerd, maar ook naar door welke uitspraken deze wordt geciteerd en hoe deze zich verhoudt tot andere uitspraken binnen het netwerk. Hierdoor verandert de analyse van een eenvoudige telling van citaties naar een meer structurele benadering van het netwerk.

Hoewel centraliteitsmaten een krachtig hulpmiddel bieden om invloed binnen netwerken te analyseren, wijzen verschillende studies op belangrijke beperkingen. Zo kunnen verschillende centraliteitsmaten leiden tot uiteenlopende resultaten. Fowler en Jeon (2008) laten zien dat het meten van invloed afhankelijk is van de gekozen methode. Zij introduceren de zogeheten *authority scores*, waarbij niet alleen het aantal citaties van een uitspraak relevant is, maar ook de kwaliteit van de uitspraken die deze citeren (Fowler & Jeon, 2008). Dit betekent dat eenvoudige maatstaven, die alle citaties als gelijk behandelen, maar een beperkt beeld geven van invloed. Verschillende manieren van meten kunnen daardoor leiden tot verschillende interpretaties van invloed binnen een netwerk.

Binnen de netwerkwetenschap is aangetoond dat veel complexe netwerken een structuur vertonen waarin de verdeling van verbindingen niet willekeurig is. Barabási en Albert (1999) tonen aan dat in schaalvrije netwerken de kans dat een knoop een groot aantal verbindingen heeft afneemt volgens een machtswet, waardoor de meeste knopen slechts weinig verbindingen hebben, terwijl een klein aantal knopen een groot aantal verbindingen heeft. Dit patroon wordt verklaard door twee mechanismen: de groei van het netwerk door toevoeging van nieuwe knopen en de *preferential attachment*, waarbij nieuwe knopen zich vaak eerder verbinden met knopen die al een groot aantal verbindingen hebben (Barabási & Albert, 1999). De combinatie van deze mechanismen leidt tot een machtswetverdeling en een schaalvrije netwerkstructuur.

Naast de keuze van centraliteitsmaten speelt ook de structuur van het netwerk als geheel een belangrijke rol. Binnen de netwerkwetenschap is uitgebreid onderzoek gedaan naar de structuur van citatienetwerken, met name in de context van wetenschappelijke publicaties. Uit deze literatuur blijkt dat de verdeling van citaties vaak sterk scheef is. Een van de eerste systematische analyses van deze verdeling is uitgevoerd door Redner (1998), die laat zien dat de *tail* van de citatiedistributie een power-law gedrag vertoont. Dit betekent dat het aantal publicaties met een groot aantal citaties langzaam afneemt volgens een machtswet, wat duidt op een sterke concentratie van citaties in een klein aantal publicaties. Bovendien blijkt uit zijn analyse dat de verdeling niet door één enkele functionele vorm kan worden beschreven over het gehele bereik van citaties, wat suggereert dat verschillende mechanismen een rol spelen in verschillende delen van de verdeling.

Later onderzoek heeft echter aangetoond dat de volledige citatiedistributie complexer is dan een simpele power law. Zo tonen Young-Ho Eom en Santo Fortunato (2011) aan dat citatienetwerken worden gekenmerkt door brede, *heavy-tailed* verdelingen en dat een shifted power law vaak een betere beschrijving geeft van de data dan een eenvoudige power law . Daarnaast laten zij zien dat citatiedynamiek wordt beïnvloed door factoren zoals tijd en “citation bursts”, wat aangeeft dat de opbouw van citaties niet gelijkmatig is.

Ondanks deze inzichten richt een groot deel van de bestaande literatuur zich vooral op het identificeren van individuele invloedrijke uitspraken, vaak door middel van ranglijsten op basis van centraliteitsmaten. Er is relatief minder aandacht voor de onderliggende verdeling van citaties en de mate van ongelijkheid binnen het netwerk. Juist deze verdeling is echter belangrijk voor het begrijpen van de structurele eigenschappen van een netwerk een de manier waarop invloed binnen een netwerk is verdeeld.

Dit onderzoek richt zich op een aspect dat in eerdere studies minder centraal staat, namelijk de verdeling van citaties binnen het netwerk als geheel. Door te onderzoeken in hoeverre citaties geconcentreerd zijn in een klein aantal uitspraken en of deze verdeling kenmerken vertoont van bekende netwerkstructuren, draagt dit onderzoek bij aan een beter begrip van de structuur van juridische citatienetwerken en de concentratie van invloed binnen het recht.



# Research question
Uit de literatuur blijkt dat juridische citatienetwerken vaak worden geanalyseerd met behulp van centraliteitsmaten, waarbij de nadruk ligt op het identificeren van individuele invloedrijke uitspraken. Tegelijkertijd laten studies binnen de netwerkwetenschap zien dat citatienetwerken vaak een sterk scheve verdeling vertonen, waarbij een klein aantal knopen een groot deel van de citaties ontvangt. Deze inzichten suggereren dat niet alleen individuele uitspraken van belang zijn, maar ook de manier waarop citaties over het netwerk als geheel zijn verdeeld.

De centrale onderzoeksvraag luidt: "*Hoe is de verdeling van citaties (in-degree) in het citatienetwerk van Rechtspraak.nl, en in hoeverre is de verdeling geconcentreerd in een klein aantal uitspraken?*"

Om deze vraag te beantwoorden, worden de volgende deelvragen geformuleerd:

1. Wat is de verdeling van het aantal ontvangen citaties (in-degree) over uitspraken in het citatienetwerk?

2. In hoeverre is de verdeling van citaties ongelijk verdeeld over uitspraken?

3. In hoeverre vertoont de in-degree distributie kenmerken van een schaalvrije (power law) verdeling?

4. Wat betekenen de gevonden patronen voor de concentratie van invloed binnen het citatienetwerk?

z
# Method and approach
Dit onderzoek past netwerkanalyse toe op Nederlandse juridische citaties, waarbij verwijzingen tussen uitspraken worden gemodelleerd als relaties binnen een netwerkstructuur. Door deze relaties systematisch te analyseren, kan inzicht worden verkregen in hoe citaties zich over het netwerk verdelen en in hoeverre deze geconcentreerd zijn in een beperkt aantal uitspraken.

De analyse is gebaseerd op een dataset waarin verwijzingen tussen juridische documenten, afkomstig van Rechtspraak.nl, zijn vastgelegd in de vorm van bron- en doel-URI’s. In de eerste stap worden deze verwijzingen ingelezen en bewerkt, waarbij de relevante onderdelen van de URI’s worden gebruikt om alle unieke uitspraken te identificeren. Omdat dezelfde uitspraak in verschillende vormen kan voorkomen, worden identifiers eerst genormaliseerd en vervolgens samengevoegd, zodat elke uitspraak slechts één keer in het netwerk voorkomt.

Vervolgens wordt het citatienetwerk gemodelleerd als een gericht netwerk, waarbij elke uitspraak wordt gemodelleerd als een knoop (node) en elke citatie als een gerichte verbinding (edge) van de citerende uitspraak naar de geciteerde uitspraak. Aangezien de dataset ook verwijzingen naar andere juridische bronnen bevat, zoals wetgeving, wordt het netwerk in deze stap beperkt tot verwijzingen tussen uitspraken onderling. Deze afbakening zorgt ervoor dat de analyse zich richt op citatiepatronen binnen de rechtspraak zelf.

De kern van de analyse richt zich vervolgens op de verdeling van in-degree. Deze wordt onderzocht met behulp van zowel statistische maten als visualisaties. Door het gebruik van grafieken wordt geanalyseerd of de verdeling kenmerken vertoont van een scheve of heavy-tailed structuur. Daarnaast wordt de mate van ongelijkheid in de verdeling gemeten door te bepalen welk deel van de citaties wordt ontvangen door de meest geciteerde uitspraken, bijvoorbeeld binnen de top 1% en top 10%.

Ten slotte wordt onderzocht in hoeverre de waargenomen verdeling overeenkomt met bekende netwerkstructuren, zoals schaalvrije netwerken. Dit gebeurt door te analyseren of de staart van de verdeling een patroon volgt dat consistent is met een power-law relatie, en door alternatieve verdelingen te overwegen als dit niet het geval is.

# Evaluation
De resultaten van dit onderzoek worden geëvalueerd aan de hand van zowel statistische analyse als vergelijking met bestaande literatuur over citatienetwerken. Hierbij wordt gekeken in hoeverre de geobserveerde verdeling van citaties overeenkomt met bekende patronen, zoals scheve of heavy-tailed verdelingen.

Allereerst wordt beoordeeld of de in-degree verdeling kenmerken vertoont van een ongelijke verdeling van citaties. Dit gebeurt op basis van visualisaties, zoals histogrammen en grafieken op logaritmische schaal. Daarnaast wordt de mate van ongelijkheid gemeten door te analyseren welk deel van de citaties wordt ontvangen door de meest geciteerde uitspraken.

Verder wordt geëvalueerd in hoeverre de data past bij verschillende theoretische verdelingen. Hierbij wordt gekeken of een power law een geschikte beschrijving biedt van de verdeling, of dat alternatieve modellen, zoals een log-normale verdeling of een shifted power law, een betere beschrijving geven van de data.

Tot slot worden de resultaten geïnterpreteerd in relatie tot bestaande studies, om te bepalen in hoeverre de gevonden patronen aansluiten bij eerder onderzoek naar citatienetwerken.


# Plan
In het eerste deel van het onderzoek wordt het literatuuronderzoek en het theoretisch kader afgerond. Hierbij worden de belangrijkste concepten en methoden vastgesteld die als basis staan voor de verdere analyse.

In de tweede fase wordt de dataset verkend en opgeschoond. Hierbij worden de relevante verwijzingen geïdentificeerd, genormaliseerd en samengevoegd, waarna het citatienetwerk wordt opgebouwd.

In de derde fase wordt het netwerk geanalyseerd. Eerst wordt een beschrijvende analyse uitgevoerd om inzicht te krijgen in de structuur van het netwerk en de verdeling van de in-degree. Vervolgens wordt de mate van ongelijkheid in de verdeling van citaties bekeken en wordt geanalyseerd in hoeverre de verdeling kenmerken vertoont van een schaalvrije structuur.

In de vierde fase worden de resultaten geïnterpreteerd en vergeleken met de bestaande literatuur. Hierbij wordt beoordeeld in hoeverre de gevonden patronen aansluiten bij eerdere studies naar citatienetwerken.

De laatste fase bestaat uit het afronden van het schrijven van de scriptie en het voorbereiden van de presentatie. Deze fase valt deels samen met de analyse, zodat resultaten direct kunnen worden verwerkt in de tekst.

# Report and presentations
De output van dit onderzoek is een schriftelijke rapportage van de resultaten. De bevindingen worden vastgelegd in de scriptie, waarin zowel de theoretische achtergrond, de methode als de resultaten en interpretaties worden beschreven. Naast de scriptie wordt ook een Jupyter Notebook opgeleverd, waarin de dataverwerking, netwerkanalyse en visualisaties zijn uitgewerkt.

