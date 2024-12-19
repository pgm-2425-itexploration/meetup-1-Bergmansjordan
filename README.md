voor mijn meetup ben ik naar de umbraco meetup gegaan waar ze uitleg gaf over de code camp en waar ze computer over de nieuwe features van umbraco

in deze proof of concept leg ik uit hoe je het beste umbraco kunt installeren met visual studio code zodat jullie het zelf kunnen doen

dit zijn de eisen
Lokale ontwikkeling
Hieronder vindt u de minimale vereisten om Umbraco 15 op uw machine te gebruiken:

.NET 9.0 en hoger

Een van de .NET 9-ondersteunde besturingssysteemversies

Een van de volgende .NET Tools of Editors:

Visual Studio Code met de IISExpress-extensie

Microsoft Visual Studio 2022 versie 17.12 of hoger.

Optioneel: JetBrains Rider versie 2022.3 en hoger

.NET Core CLI

SQL-verbindingsreeks (SQL Server)

Node.js versie 20.11.0 en hoger

moest ik dit doen zou ik zeker deze items goed volgen want anders ga je in problemen komen net zoals ik heb gehad.

maak dat je .net geinstalleerd hebt op deze site: https://dotnet.microsoft.com/en-us/download/visual-studio-sdks

Klik linksonder op het extensiemenu. Zoek vervolgens naar C# en installeer het.


VS Code-installatie-extensie
Creëer uw Umbraco-project
Volg de Sjablonengids om uw projectmap te maken.

Configureer VS Code om het Umbraco-project uit te voeren
Open uw projectmap in VS Code, uw project zal er ongeveer zo uitzien:


Verse Umbraco installatie
Nu moeten we VS Code vertellen hoe u uw project moet uitvoeren.

Open het opdrachtenpalet, u kunt de sneltoets Ctrl+Shift+P gebruiken en Taken: Configureren typen en de optie Taken: Taak configureren selecteren:

Taakoptie configureren
Selecteer "Taak.json maken van sjabloon"

Taak maken van sjabloon
Selecteer nu " .NET Core" als uw sjabloon.

Maak .NET Core-sjabloon
Hierna zal VS Code een map genaamd .vscode hebben gemaakt die een bestand genaamd tasks.json bevat, het is dit bestand dat VS Code vertelt hoe uw project moet worden gebouwd.

Nu we 'heb VS Code verteld hoe je project te bouwen, wij moeten het vertellen hoe het te lanceren. VS Code kan dit voor je doen. Selecteer eerst de kleine play-knop in het linkermenu en selecteer vervolgens 'maak een lancering' .json-bestand"-link.

Het bestand launch.json maken
Hierdoor verschijnt er een menu, selecteer .NET 5+ en .NET Core:

Promptmenu
Als .NET 5+ en .NET Core ontbreken in het vervolgkeuzemenu:

Druk op Ctrl + Shift + P ( op Windows/Linux) of Cmd + Shift + P (op macOS) om het Command Palette te openen.

Zoek naar de opdracht .NET: Generate Assets for Build and Debug. Deze opdracht genereert de benodigde assets voor het bouwen en debuggen van uw .NET-applicatie .

Nu ziet u een groene afspeelknop verschijnen met een dropdown waar ".NET Core Launch (web)" is geselecteerd.

Opties voor de groene afspeelknop
Als u naar de sectie Bestanden navigeert, wordt er een nieuw bestand launch.json gemaakt in de . vscode-map. Wanneer u op F5 drukt, vertelt het bestand launch.json VS Code om uw project te bouwen, uit te voeren en vervolgens een browser te openen.

bestand launch.json
Daarmee bent u klaar om het project uit te voeren! Druk op F5 of klik op de kleine groene afspeelknop in de sectie Uitvoeren en debuggen om uw gloednieuwe Umbraco-site lokaal uit te voeren.

Umbraco Web Installer
Deze sectie gaat verder waar we gebleven waren, maar behandelt de installatie en configuratie van Umbraco in uw webbrowser wanneer u Umbraco voor de eerste keer uitvoeren.

U ziet het installatiescherm waar u wat gegevens moet invullen voordat Umbraco kan worden geïnstalleerd.

Web Installer - Laten we beginnen
Wanneer de installer klaar is, wordt u ingelogd in de backoffice.

Gefeliciteerd, je hebt een Umbraco-site geïnstalleerd!

Aan de slag
De tutorial Een basissite maken biedt stapsgewijze instructies om een ​​Umbraco-website te bouwen met behulp van een set HTML-, CSS- en JavaScript-bestanden. Deze tutorial stelt je in staat om een ​​websitesjabloon te gebruiken, en verbind de secties die content management vereisen in het Umbraco CMS.

Wat u nodig hebt
Om deze tutorial te beginnen, moet u de Custom Umbraco Template downloaden. Als u op de link klikt, worden de bestanden automatisch naar uw apparaat gedownload.

Umbraco installeren
Om de nieuwste versie van Umbraco te downloaden, raadpleegt u het artikel Installatie. Volg de stappen in de installatiewizard:

Voer uw naam, e-mailadres en wachtwoord in.

Umbraco installeren
Klik op Volgende.

Kies het niveau van toestemming voor telemetriegegevens voor uw Umbraco installatie.

Klik op Volgende.

Selecteer het Database Type uit de vervolgkeuzelijst.

Voer de Database Naam in.

Klik op Installeren.

De installatie duurt een paar minuten.

De Custom Umbraco Template Site voorbereiden
Pak de Custom Umbraco Template uit naar een map op uw systeem. Als u op de link klikt, worden de bestanden automatisch naar uw apparaat gedownload.

Open de index.html in de map in uw favoriete browser om de sjabloon te bekijken.

Standaard sjabloonhomepage
De sjabloon bevat wat tekst met dummy-links. We gaan dit omzetten in een volwaardige, Umbraco-aangedreven site!

Inloggen op Umbraco
U kunt op twee manieren inloggen op Umbraco:

Zodra de installatie is voltooid, ziet u het inlogscherm.

Nlde naam en het wachtwoord die tijdens het installatieproces worden gebruikt.

Documenttypen
De eerste stap bij het maken van een Umbraco-site is het instellen van een documenttype. Een documenttype fungeert als een gegevenscontainer in Umbraco, waar u eigenschappen (gegevensvelden of kenmerken) kunt toevoegen om inhoud op te slaan. Aan elke eigenschap wordt een gegevenstype toegewezen, zoals een tekstreeks, nummer of rich text-editor. Umbraco gebruikt sjablonen om deze invoergegevens op de front-end weer te geven.

Hier zijn enkele van de meest voorkomende eigenschappen die u in een documenttype kunt toevoegen:

Paginatitel

Subkop

Hoofdtekst

Metatitel

Metabeschrijving

Een documenttype maken
Om een ​​documenttype te maken:

Ga naar Instellingen.

Klik op ... naast de documenttypen.

Selecteer Maken...

Selecteer Documenttype met sjabloon.

Mappen kunnen u helpen uw documenttypen te organiseren.

Een documenttype maken met sjabloon
Voer een naam in voor het documenttype. Laten we het Startpagina noemen. U zult merken dat er automatisch een alias wordt gemaakt.

De alias van het Documenttype wordt automatisch gegenereerd op basis van de eigenschapsnaam. Als u de automatisch gegenereerde alias wilt wijzigen, klikt u op het pictogram 'slot'. De alias moet in camelcase staan. Bijvoorbeeld homePage.

Klik op Opslaan. Ons nieuwe Documenttype is nu zichtbaar als een nieuw item onder Documenttypen.

Een documenttype opslaan
Het documenttype aanpassen
Pictogrammen toevoegen
Met behulp van pictogrammen kunt u verschillende documenttypen identificeren in de inhoudsboom. Om een ​​pictogram toe te voegen:

Klik op de pictogram-placeholder naast de documentnaam. Het dialoogvenster Pictogram selecteren wordt geopend.

Een pictogram selecteren
Blader door de pictogramlijst en selecteer het pictogram van uw keuze.

Klik op Verzenden.

Klik op Opslaan.

Machtigingen instellen
Om een ​​documenttype te maken in de root van de inhoudsboom:

Ga naar het tabblad Structuur.

Schakel de knop Toestaan ​​bij root in.

Documenttype toestaan ​​als root
Als Toestaan ​​bij root niet is ingeschakeld op het documenttype, kunt u geen inhoud op uw site maken.

Klik op Opslaan.

Eigenschappen toevoegen
Volg deze stappen om eigenschappen toe te voegen aan uw documenttype:

Ga naar het tabblad Ontwerp.

Klik op Groep toevoegen.

Voer een naam in voor de groep. Voor deze tutorial noemen we het Inhoud.

Groep toevoegen
Klik op Eigenschap toevoegen. Het dialoogvenster Eigenschap toevoegen wordt geopend.

Voer een naam in. Bijvoorbeeld: Paginatitel.

Voer een beschrijving in. Bijvoorbeeld: De hoofdtitel van de pagina (Welcome to Widgets Ltd.).

Eigenschap toevoegen
Klik op Eigenschappeneditor selecteren.

Selecteer het gewenste gegevenstype. We voegen tekst toe in het zoekvak en selecteren het gegevenstype Tekstreeks.

Gegevenstype selecteren
Klik op Verzenden.

Vergeet niet om later terug te komen en de lijst met gegevenstypen te bekijken.

Herhaal stap 4 tot en met 9 om een ​​hoofdtekst toe te voegen met behulp van de onderstaande specificatie:

Naam
Hoofdtekst
Beschrijving

De hoofdinhoud van de pagina.

Gegevenstype

Richtext-editor

Klik op Groep toevoegen om een ​​nieuwe groep te maken met de naam Voettekst. Herhaal stap 4 tot en met 9 om een ​​voettekst toe te voegen met behulp van de onderstaande specificatie:

Naam
Voettekst
Beschrijving

Copyrightkennisgeving voor de voettekst.

Gegevenstype

Tekstreeks

Uw documenttype zou er nu zo uit moeten zien:

Klik op Opslaan.

Startpagina met eigenschappen
We hebben nu ons eerste documenttype gemaakt. Umbraco haalt de gegevens uit een exemplaar van het documenttype (ook wel Content Node genoemd). Deze gegevens worden vervolgens samengevoegd met een sjabloon. Laten we nu onze sjabloon maken.

Uw eerste sjabloon maken
Umbraco maakt een bijbehorende sjabloon wanneer u de optie Documenttype met sjabloon selecteert bij het maken van een documenttype.

Om de sjabloon te bewerken:

Ga naar Instellingen.

Vouw de map Sjablonen uit in het gedeelte Sjablonen van de boom. U zou een sjabloon moeten zien met de titel Startpagina.

Als u de sjabloon niet ziet, probeer dan de pagina te vernieuwen.

Open de sjabloon. Deze bevat een klein beetje Razor-code.

Code-indeling:

@using Umbraco.Cms.Web.Common.PublishedModels; - Importeert de naamruimte voor Umbraco's sterk getypeerde inhoudsmodellen.

@inherits Umbraco.Cms.Web.Common.Views.UmbracoViewPage - Stelt de weergave in om te erven van Umbraco's basisweergaveklasse voor toegang tot Umbraco-specifieke functies en helpers.

Layout = "null"; - De weergave gebruikt geen lay-outpagina, tenzij expliciet gespecificeerd. Raadpleeg de Microsoft-documentatie voor meer informatie over Razor Pages Layout.

Startpaginasjabloon
Plak de sjablooncode, maar laat de code die er al is staan.

We gebruiken de bestanden uit de map Aangepaste Umbraco-sjabloon. Als u op de koppeling klikt, worden de bestanden automatisch gedownload naar uw apparaat.

Open de map Aangepaste Umbraco-sjabloon en kopieer de inhoud van index.html.

Plak de inhoud in de Startpaginasjabloon onder de sluitende accolade "}".

Umbraco Templates gebruikt Razor waarmee u code kunt toevoegen aan uw Template-bestanden. Razor reageert op @-tekens.

Klik op Opslaan.

We hebben nu een Template. Dat zijn twee van de drie voltooide fasen voor onze eerste pagina.

Uw eerste contentnode maken
Onze derde en laatste fase voor het maken van onze eerste pagina in Umbraco, is het maken van een contentnode. De contentnode gebruikt ons Documenttype en Template om een ​​HTML-pagina aan webbezoekers te presenteren.

Om een ​​contentnode toe te voegen:

Ga naar Content.

Selecteer ... naast Content in de boom.

Klik op Maken.

Selecteer Startpagina. De startpagina wordt geopend in de inhoudseditor.

Als u het inhoudsknooppunt niet kunt zien, controleer dan of Instellingen > Documenttypen > Startpagina > Structuur > Toestaan ​​bij root is ingeschakeld.

Inhoudsknooppunt Startpagina
Voer de naam in voor het inhoudsknooppunt. We noemen dit Startpagina.

De naam wordt weergegeven in de knooppuntenlijst en wordt gebruikt om een ​​URL voor de pagina te maken. Probeer het kort maar beschrijvend te houden.

Voer de volgende gegevens in:

Naam
Beschrijving
Paginatitel

Welkom bij Widgets Ltd

Hoofdtekst

Lorem ipsum

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam et aliquet ante, ut eleifend libero.

Proin eleifend consequat nunc id vulputate.

Ut eget lobortis metus, non congue lorem.

Orci varius natoque penatibus en magnis dis parturient montes, nascetur ridiculus mus.

Maecenas tempus non lectus rhoncus efficitur.

Sed est ligula, maximus in dolor sed, lacinia egestas ligula. Donec eu nisi lectus.

Er is sprake van een niet-ernstige ziekte.

Voettekst

Copyright Widgets Ltd 2024

Klik op Opslaan en publiceren. De inhoudsboom wordt opnieuw geladen met het startpuntknooppunt.


Startpagina in inhoudsboom
Toegang tot de frontend
Om uw inhoud op de frontend te bekijken:

Ga naar het tabblad Info in het inhoudsknooppunt Homepage.

Klik op de link onder het kopje Links.

De standaard Umbraco-pagina is verdwenen en we kunnen een eenvoudige, ongestylede pagina zien. We komen er.

Als u een lege pagina ziet, controleer dan of de sjabloon is ingevoerd en vergeet niet deze op te slaan.

CSS en afbeeldingen
Onze homepage mist momenteel de CSS- en afbeeldingsbestanden. Om deze bestanden op te nemen:

Ga naar de map MyCustomUmbracoProject en de map Custom Umbraco Template in Verkenner.

Kopieer de mappen css en images uit de map Custom Umbraco Template en plaats deze in de map wwwroot in de map MyCustomUmbracoProject.

Ga naar de HomePage-sjabloon in het gedeelte Instellingen en zorg ervoor dat de verwijzingslink naar het stylesheet /css/main.css is.

Verwijzing naar het stylesheet
Start of vernieuw met Chrome/Firefox/Edge Developer Tools uw http://localhost:xxxx.

Het tabblad netwerk mag geen ontbrekende CSS- of afbeeldingsbestanden melden. Als het tabblad netwerk een fout meldt, controleer dan op typefouten en of de mappen op de juiste plaatsen staan.

De eigenschappen van het documenttype weergeven
U hebt misschien gemerkt dat de inhoud die we aan de homepage hebben toegevoegd, niet wordt weergegeven. We moeten de eigenschappen van het gegevenstype koppelen aan de sjabloon.

Laten we naar onze sjabloon kijken en bepalen waar de inhoud moet worden weergegeven.

Waar onze gegevenseigenschappen moeten worden uitgevoerd
De bovenste pijl in deze afbeelding is de paginatitel en de onderste pijl is de hoofdtekst. De voettekst staat helemaal onderaan de pagina.

De documenttype-eigenschappen instellen
Om de documenttype-eigenschappen in te stellen:

Ga naar Instellingen.

Open de startpaginasjabloon.

Scrol omlaag naar het gedeelte <!-- Jumbotron, w title --> (ongeveer regel 45) en markeer de tekst "Welcome - UmbracoTV" (ongeveer regel 48).

Vervang de waarde van de paginatitel
Klik op Invoegen en selecteer Waarde.

Selecteer Documenttype in de vervolgkeuzelijst Veld kiezen.

Selecteer Startpagina.

Klik op Kiezen.

Selecteer het veld pageTitle in de vervolgkeuzelijst Startpagina.

Veld Paginatitel
Klik op Verzenden.

Ga naar de inhoud tussen de <div class="container">-tags (ongeveer regel 60 tot 77):

Markeer de inhoud zoals weergegeven in de afbeelding.

Vervang de waarde van de hoofdtekst
Herhaal stappen 4 tot en met 9 om het veld bodyText in te voegen.

Ga naar de inhoud tussen de tag <div class="container-fluid footer"> (rond regel 148 tot en met 181):

Markeer de inhoud tussen de tags <div class="container">.

Vervang de waarde van de voettekst
Herhaal stappen 4 tot en met 9 om het veld footerText in te voegen.

Klik op Opslaan.

Laad uw startpagina opnieuw om de inhoud te bekijken. U zou iets moeten zien dat lijkt op de onderstaande afbeelding:

Documenttype-eigenschappen weergeven
Nu kunt u teruggaan en extra velden toevoegen of bestaande velden in het documenttype bijwerken. Vul ze in het inhoudsknooppunt in en voeg ze vervolgens toe aan de sjabloon om de gegevens op de website weer te geven.

Een hoofdsjabloon maken
We hebben gezien hoe u een documenttype en de bijbehorende sjabloon maakt. Als u een website wilt maken met de pagina's Home, Nieuws en Contact, moet u een documenttype met een bijbehorende sjabloon maken.

Het kan zijn dat u dezelfde HTML-code in elk van deze sjablonen kopieert, wat tijdrovend en repetitief kan zijn. In een dergelijk scenario kunt u overwegen om een ​​nieuwe hoofdsjabloon te maken.

Om een ​​nieuwe hoofdsjabloon te maken:

Ga naar Instellingen.

Selecteer de ... naast de map Sjablonen. U kunt ook op + klikken om een ​​lege sjabloon te openen.

Klik op Maken. Er wordt een sjabloon geopend in de inhoudseditor.

Voer een naam in voor de hoofdsjabloon. Laten we deze Hoofd noemen.

Hoofdsjabloon
Klik op Opslaan.

De hoofdsjabloon gebruiken
Om de hoofdsjabloon te gebruiken:

Ga naar Instellingen.

Vouw de map Sjablonen uit in het gedeelte Sjablonen.

Open de sjabloon Startpagina.

Selecteer Hoofdsjabloon: Geen hoofdsjabloon. Het dialoogvenster Hoofdsjabloon wordt aan de rechterkant van de browser geopend.

Selecteer de sjabloone genaamd Master.

Klik op Kiezen. De Razor-codesectie wordt bijgewerkt van Layout = null; naar Layout = "Master.cshtml";

Master-sjabloon toevoegen aan de startpagina
Klik op Opslaan.

Sjablonen bijwerken met de nieuwe master-sjabloon
We moeten nu de onderdelen van onze HTML-sjabloon die in alle sjablonen voorkomen, verplaatsen naar de master. Het kan voor verschillende websites enigszins verschillen. U moet overwegen of alle pagina's een <div id="main">-sectie bevatten, zodat u deze in de master kunt bijwerken.

Volg deze stappen om sjablonen bij te werken met de nieuwe master-sjabloon:

Ga naar Instellingen.

Vouw de map Sjablonen uit in de sectie Sjablonen.

Navigeer naar de startpagina-sjabloon.

Knip alles van de <!DOCTYPE HTML> (rond regel 7) tot het einde van de </div>-tag (rond regel 43), wat de header en navigatie van de site naar de master-sjabloon is.

Header- en navigatietags geselecteerd in de startpagina-sjabloon
Klik op Opslaan.

Ga naar de Master-sjabloon en plak deze HTML-opmaak na de afsluitende accolade (rond regel 7).

Header- en navigatietags toegevoegd in de Master-sjabloon
Voeg @RenderBody() toe aan het einde van de opmaak. Dit vertelt Umbraco om de inhoud van de onderliggende sjabloon in te voegen.

Renderbody toevoegen in de Master-sjabloon
Klik op Opslaan.

Herhaal hetzelfde proces voor de inhoud van de voettekst:

Ga naar de Homepage-sjabloon en knip alles van de <!-- Footer -->-tag (rond regel 108) tot het einde van de </html>-tag (rond regel 122) en klik op Opslaan.

Ga naar de Master-sjabloon en plak deze HTML-opmaak na het veld @RenderBody() dat we hebben toegevoegd.

Einde van de Master-sjabloon
Klik op Opslaan.

Nu hebben we veel werk gedaan. Wanneer we onze localhost-pagina vernieuwen, is er niets veranderd. Als u een compilatiefout hebt, hebt u misschien @RenderBody() verkeerd getypt.

Pagina's maken en de hoofdsjabloon gebruiken
Een contactpagina maken
We gaan nu een pagina maken om onze contactgegevens weer te geven. Voor extra functionaliteit kunt u overwegen deze pagina te vervangen door een volledig 'Contact'-formulier.

Hier zijn enkele mogelijke oplossingen:

Gebruik Umbraco Forms (voor niet-ontwikkelaars): Umbraco biedt een add-on genaamd Umbraco Forms. Deze tool is ideaal voor gebruikers die geen programmeurs zijn, omdat editors hiermee aangepaste formulieren kunnen maken. U kunt meer informatie vinden en het product kopen op Umbraco.com.

Bouw uw eigen contactformulier (voor ontwikkelaars): Als u de voorkeur geeft aan een aangepaste oplossing, kunt u uw eigen contactformulier maken met behulp van Surface Controllers in Umbraco.

Het documenttype en de sjabloon maken
Volg deze stappen om een ​​contactpagina met alleen inhoud in Umbraco te maken:

Ga naar Instellingen.

Klik op ... naast Documenttypen.

Selecteer Maken. Het dialoogvenster Documenttype maken wordt geopend.

Selecteer Documenttype met sjabloon.

Selecteer een pictogram uit de lijst met pictogrammen.

Klik op Verzenden.

Voer een naam in. Noem het Simple Content Page.

Voeg twee velden toe met de volgende specificaties:

Groep
Veldnaam
Alias
Gegevenstype
Inhoud

Paginatitel

paginatitel

Tekstreeks

Inhoud

Hoofdtekst

bodyText

Rich Text Editor

Sjabloon voor Simple Content Page met gegevensvelden
Klik op Opslaan.

Ga naar Sjablonen om uw sjabloon voor Simple Content Page te bekijken die automatisch is gemaakt met het documenttype.

Als u de sjabloon niet ziet, probeer dan de pagina te vernieuwen.

Open de sjabloon voor Simple Content Page.

Selecteer Hoofdsjabloon: Geen hoofdsjabloon en kies de hoofdsjabloon.

Klik op Kiezen.

Voeg de volgende HTML toe na de afsluitende }.

Kopiëren
<!-- Jumbotron, w title -->
<div class="jumbotron text-center jumbotron-fluid">
<div class="container">
<h1 class="display-1">Umbraco-ondersteuning</h1>
</div>
</div>

<!-- Hoofdpagina -->
<section id="main" class="wrapper">
<div class="container">

<p>Bent u een ontwikkelaar?</p>
<p>Bent u een marketeer?</p>
<p>Werk je bij een bureau?</p>
<p>Laat Umbraco uw talent ontketenen</p>
</div>
</section>
Klik op Opslaan.

De machtigingen voor het documenttype bijwerken
We moeten nu de machtigingen voor het documenttype bijwerken om specifiek onderliggende knooppunten toe te voegen onder het hoofdinhoudsknooppunt.

Om de machtigingen voor het documenttype bij te werken:

Ga naar Instellingen.

Open het startpaginadocumenttype.

Ga naar het tabblad Structuur.

Klik op Kiezen in de Toegestane onderliggende knooppunttypen.

Selecteer Eenvoudige inhoudspagina.

Sta onderliggende knooppunten toe op de startpagina
Klik op Kiezen.

Klik op Opslaan.

Het inhoudsknooppunt maken
Om een ​​inhoudsknooppunt te maken:

Ga naar Inhoud.

Selecteer ... naast het startpaginaknooppunt.

Klik op Maken.

Selecteer Eenvoudige inhoudspagina.

Inhoudspagina toevoegen als onderliggend knooppunt
Voer een naam in voor het documenttype. Noem het Contact opnemen.

Vul details in voor de paginatitel en hoofdtekst.

Klik op Opslaan en publiceren.

De documenttype-eigenschappen toevoegen
Om de documenttype-eigenschappen toe te voegen:

Ga naar Instellingen.

Vouw de map Sjablonen uit in het gedeelte Sjablonen.

Ga naar Master en open de sjabloon Eenvoudige inhoudspagina.

Scrol naar het gedeelte <!-- Jumbotron, w title --> (rond regel 7) en markeer de tekst "Umbraco Support" (rond regel 10).

Klik op Invoegen en selecteer Waarde.

Selecteer Documenttype uit dee Kies veld vervolgkeuzelijst.

Selecteer Eenvoudige inhoudspagina.

Klik op Kiezen.

Selecteer paginatitel in de vervolgkeuzelijst Eenvoudige inhoudspagina.

Klik op Verzenden.

Herhaal hetzelfde proces voor de <div class="container">-tag:

Markeer de inhoud van de <p>-tag (rond regel 18) tot het einde van de </p>-tag (rond regel 21).

Klik op Invoegen en selecteer Waarde.

Selecteer Documenttype in de vervolgkeuzelijst Kies veld.

Selecteer Eenvoudige inhoudspagina.

Klik op Kiezen.

Selecteer bodyText in de vervolgkeuzelijst Eenvoudige inhoudspagina.

Klik op Verzenden.

Klik op Opslaan.

De pagina Contact opnemen bekijken
Om de pagina Contact opnemen te bekijken:

Ga naar Inhoud.

Navigeer naar de pagina Contact opnemen.

Ga naar het tabblad Info.

Klik op de link om de pagina te bekijken.

Pagina Contact opnemen bekijken
Documenttype-eigenschappen gebruiken vanaf de startpagina
U ziet misschien dat de voettekst nu leeg is - we hebben geen inhoud van ons startpaginaknooppunt.

Ga als volgt te werk om de Documenttype-eigenschappen van het startpaginadocumenttype te gebruiken:

Ga naar Instellingen.

Vouw de map Sjablonen uit in het gedeelte Sjablonen.

Open de hoofdsjabloon.

Markeer @Model.Value("footerText") in de voettekst (rond regel 51).

Klik op Invoegen en selecteer Waarde.

Selecteer Documenttype in de vervolgkeuzelijst Veld kiezen.

Selecteer Startpagina.

Klik op Kiezen.

Selecteer het veld footerText in de vervolgkeuzelijst Startpagina.

Selecteer het selectievakje Ja, maak het recursief. Dit geeft Umbraco de melding om de inhoudsboom op te zoeken als het veld niet bestaat op het knooppuntniveau voor de pagina die we opvragen.

Klik op Verzenden.

Klik op Opslaan.

Laad de pagina Contact opnemen opnieuw om de inhoud met de voettekst te bekijken.

Het navigatiemenu instellen
U kunt het navigatiemenu op twee manieren instellen:

Dynamisch: Umbraco kan automatisch een navigatiemenu genereren op basis van de pagina's in de inhoudsboom. Wanneer u een pagina maakt of wijzigt, wordt deze automatisch weergegeven in het navigatiemenu. Deze dynamische aanpak elimineert de noodzaak om handmatig menu-items toe te voegen of bij te werken wanneer pagina's worden toegevoegd, verwijderd of hernoemd.

Hardcoded: U kunt het navigatiemenu ook hardcoderen. Deze aanpak vereist echter meer onderhoud, omdat alle wijzigingen aan de pagina's, zoals toevoegen, verwijderen of hernoemen, handmatig in het menu moeten worden weerspiegeld.

Dynamische navigatie
Volg deze stappen om dynamische navigatiekoppelingen te maken vanuit de gepubliceerde inhoudsknooppunten:

Ga naar Instellingen.

Vouw de map Sjablonen uit in het gedeelte Sjablonen.

Open de hoofdsjabloon.

Zoek de tag <!-- Navigatie --> (rond regel 20).

Plaats de cursor er direct onder op een lege regel.

Selecteer Querybuilder... in de rechterbovenhoek van de editor.

Zorg ervoor dat het is ingesteld op "Ik wil alle inhoud van mijn website".

Klik op Verzenden.

U hebt nu het volgende fragment in uw hoofdsjabloon:

Kopiëren
@{
var selection = Umbraco.ContentAtRoot().FirstOrDefault()
.Children()
.Where(x => x.IsVisible());
}
<ul>
@foreach (var item in selection)
{
<li>
<a href="@item.Url()">@item.Name()</a>
</li>
}
</ul>
Dit fragment moet worden samengevoegd met de navigatie erboven.

Wikkel de <ul>-tag in de <div class="container">- en <nav>-tags.

Het uiteindelijke resultaat ziet er als volgt uit:

Kopiëren
@{
var selection = Umbraco.ContentAtRoot().FirstOrDefault()
.Children()
.Where(x => x.IsVisible());
}
<div class="container">
<nav class="navbar navbar-expand navbar-light">
<a class="navbar-brand font-weight-bold" href="index.html">UmbracoTV</a>
<!-- Links -->
<ul class="navbar-nav">
@foreach (var item in selection)
{
<li class="nav-item">
<a href="@item.Url()" class="nav-link">@item.Name()</a>
</li>
}
</ul>
</nav>
</div>
Klik op Opslaan.

Hardcode Navigatie
Om een ​​basis hardcoded navigatie toe te voegen, volgt u deze stappen:

Ga naar Instellingen.

Vouw de map Sjablonen uit in de sectie Sjablonen.

Open de Master-sjabloon.

Ga naar de tag <!-- Navigatie --> (rond regel 20).

Kopieer de inhoud binnen de <div>-tags (rond regel 21 tot 43) en vervang deze door de volgende code:

Kopiëren
<div class="container">
<nav class="navbar navbar-expand navbar-light">
<a class="navbar-brand font-weight-bold" href="/">Umbraco TV</a>
<!-- Links -->
<ul class="navbar-nav">
<li class="nav-item">
<a class="nav-link" href="/contact-us">Neem contact met ons op</a>
</li>
<li class="nav-item">
<a class="nav-link" href="/articles">Artikelen</a>
</li>
</ul>
</nav>
</div>
Klik op Opslaan.

De IsVisible()-helpermethode

Als u een checkbox-eigenschap toevoegt aan een documenttype met een alias van umbracoNaviHide, kan de IsVisible()-helpermethode worden gebruikt om deze uit te sluiten van weergave in een verzameling.

Laten we het menu testen. U zult merken dat klikken op de link Artikelen een Umbraco-fout oplevert, omdat we deze pagina nog niet hebben gemaakt.

Artikelen en artikelitems
Een bovenliggende pagina met onderliggende pagina's is een goed voorbeeld van de functies van Umbraco. Ons fictieve bedrijf, Widgets Ltd, publiceert bijvoorbeeld ongeveer tien artikelen per maand en wil daarom dat de bovenliggende pagina functioneert als een blog. Deze opstelling werkt voor artikelen, berichten en othaar collecties die meerdere content items vereisen op basis van hetzelfde content type.

Artikelen en Artikel Items maken
Maak twee nieuwe Document Types met template: Articles Main en Articles Item.

Om Articles Main Document Type te maken, volgt u deze stappen:

Ga naar Instellingen.

Klik op ... naast de Document Types in de Settings tree.

Selecteer Create....

Selecteer Document Type met Template.

Voer een Naam in voor het Document Type. Noem het Articles Main.

Laten we twee velden toevoegen met de volgende specificaties:

Groep
Veld Naam
Alias
Gegevens Type
Intro

Articles Title

articlesTitle

Textstring

Intro

Articles Body Text

articlesBodyText

Rich Text Editor

Articles Main Document Type Data Eigenschappen
Klik op Opslaan

Om Articles Item Document Type te maken, volgt u deze stappen:

Ga naar Instellingen.

Klik op ... naast de Document Types in de Settings tree.

Selecteer Create....

Selecteer Document Type met Template.

Voer een Naam in voor het Document Type. Noem het Articles Item.

Voeg twee velden toe met de volgende specificaties:

Group
Field Name
Alias
Data Type
Content

Article Title

articleTitle

Textstring

Content

Article Content

articleContent

Rich Text Editor

Article Item Document Type Data Properties
Klik op Save

Updating the Document Type Permissions
Om Articles Main toe te voegen als een child node:

Navigeer naar het Home Page Document Type.

Ga naar het tabblad Structure.

Selecteer Choose in de Allowed child node types.

Selecteer Articles Main.

Klik op Choose.

Klik op Save.

Om Articles Main Document Type permissions bij te werken:

Navigeer naar het Articles Main Document Type.

Ga naar het tabblad Structure.

Selecteer Choose in de Allowed child node types.

Selecteer Articles Item.

Klik op Choose.

Child Node toevoegen
Klik op Configureren als collectie.

Selecteer Lijstweergave - Inhoud.

Klik op Opslaan.

Collectie inschakelen
De Content Node maken
Om een ​​content node toe te voegen:

Ga naar Inhoud.

Selecteer ... naast de HomePage node.

Klik op Maken.

Selecteer Artikelen Hoofd.

Voer de naam voor het artikel in. We noemen het Artikelen.

Voer de inhoud in de velden Artikeltitel en Artikeltekst in.

Klik op Opslaan en publiceren. Wanneer u op Opslaan en publiceren klikt, ziet u dat er een lege collectie is gemaakt.

We moeten nog steeds de child nodes toevoegen die in de collectie worden weergegeven, zodat ze gemakkelijker te bekijken zijn. U kunt nieuwe nodes maken vanuit deze sectie.

Als u de collectie niet ziet, probeer dan de pagina te vernieuwen.

Klik op Artikelenitem maken.

Voer de naam voor het artikel in. We noemen het Artikel 1.

Voer de inhoud in de velden Artikeltitel en Artikelinhoud in.

Herhaal stap 8 tot en met 10 om artikel 2 te maken.

Klik op Opslaan en publiceren.

Inhoudsboom met artikelen
De sjabloon bijwerken
Volg deze stappen om de sjabloon Articles Main bij te werken:

Ga naar Instellingen.

Vouw de map Sjablonen uit in het gedeelte Sjablonen.

Open de sjabloon Articles Main.

Selecteer Master in het veld Master template:No Master.

Klik op Kiezen.

Klik op Opslaan.

Open de map Aangepaste Umbraco-sjabloon.

Kopieer de inhoud van Blog.html.

Plak de inhoud in Articles Main onder de sluitende accolade "}".

Verwijder alles van de <html> (rond regel 8) tot het einde van de </div>-tag (rond regel 43), wat de header en navigatie van de site is, aangezien deze al in de Master-sjabloon wordt genoemd.

Verwijder alles van de <!-- Footer --> tag (rond regel 83) tot het einde van de </html> tag (rond regel 130)

Vervang de statische tekst binnen de <h1> tags (rond regel 12) door de Model.Value verwijzing naar articlesTitle.

Vervang de statische tekst binnen de <div> tags (van regel 23 tot 29) door de Model.Value verwijzing naar articlesBodyText.

Articles Main Template
Definieer een query voor alle artikelen onder de <h3> tag (rond regel 30) van de <!-- Latest blog posts --> sectie.

Query Builder
U kunt voorwaarden instellen om specifieke artikelen te krijgen of de volgorde van de artikelen te bepalen. Voor het doel van deze handleiding gebruiken we de volgende parameters:

Query parameters
Als u de juiste parameters hebt ingesteld, krijgt u een voorbeeld van de items die met de query worden geselecteerd.

Klik op Verzenden.

U ziet een soortgelijk codefragment toegevoegd aan uw sjabloon:

Kopiëren
@{ var selection =
Umbraco.Content(Guid.Parse("56aa9cc5-243b-4947-8fb1-37b209b97373"))
.ChildrenOfType("articlesItem") .Where(x => x.IsVisible())
.OrderByDescending(x => x.CreateDate); }
<ul>
@foreach (var item in selection) {
<li>
<a href="@item.Url()">@item.Name()</a>
</li>
}
</ul>
De bovenstaande code zal een lijst van alle artikelitems als links met de naam uitgeven.

We zullen de sjabloon een beetje aanpassen om meer informatie over de artikelen toe te voegen.

Vervang de HTML in de foreach-lus met dit fragment:

Kopiëren
<article class="special">
<div class="articledate" > @item.CreateDate </div>
<div class="articletitle"><a href="@item.Url()">@item.Name()</a></div>
<div class="articlepreview">@Html.Truncate(item.Value("articleContent").ToString(), 20, true)<a href="@item.Url()">Lees @item.Name().</a></div>
</article>
Rverwijder de <ul>-tags rond de foreach-lus.

Klik op Opslaan.

Volg deze stappen om de Articles Item-sjabloon bij te werken:

Ga naar Instellingen.

Vouw de map Sjablonen uit in de sectie Sjablonen.

Open de Articles Item-sjabloon.

Selecteer Master in het veld Master template:No master.

Klik op Kiezen.

Klik op Opslaan.

Open de map Aangepaste Umbraco-sjabloon.

Kopieer de inhoud van Blogpost.html.

Plak de inhoud in Articles Item onder de sluitende accolade "}".

Verwijder alles van de <html> (rond regel 8) tot het einde van de </div>-tag (rond regel 43), wat de header en navigatie van de site is, aangezien deze al in de Master-sjabloon wordt genoemd.

Verwijder alles van de <!-- Footer --> tag (rond regel 113) tot het einde van de </html> tag (rond regel 160)

Vervang de statische tekst binnen de <h1> tags (rond regel 13) met de Model.Value verwijzing naar articleTitle.

Vervang de statische tekst binnen de <div> tags (van regel 25 tot 39) met de Model.Value verwijzing naar articleContent.

Articles Item Template
Klik op Verzenden.

Klik op Opslaan.

Taalvarianten toevoegen
Nu we een basissite-instelling hebben, maken we deze meertalig door inhoudsvariaties in een andere taal te maken. In deze tutorial maken we een Deense versie van de startpagina.

Een nieuwe taal toevoegen
Volg deze stappen om een ​​nieuwe taal toe te voegen:

Ga naar het gedeelte Instellingen.

Ga naar Talen.

Klik op Maken.

Selecteer een taal uit de vervolgkeuzelijst. In deze tutorial kiezen we Deens.

In Instellingen, om de nieuwe taal in te stellen als:

Standaardtaal voor uw site, schakel Standaardtaal in.

Verplichte taal voor uw site, schakel Verplichte taal in.

Selecteer een Fallback-taal in de vervolgkeuzelijst.

Klik op Verzenden.

Klik op Opslaan.

Een taal toevoegen
Taalvarianten inschakelen voor documenttypen en eigenschappen
Volg deze stappen om taalvarianten in documenttypen in te schakelen:

Ga naar het gedeelte Instellingen.

Selecteer Startpagina in de map Documenttypen.

Ga naar het tabblad Instellingen en schakel Variatie per cultuur toestaan ​​in

Variatie per cultuur inschakelen
Klik op Opslaan.

Ga naar het tabblad Ontwerp.

Klik op het gegevenstype van de paginatitel en schakel Variatie per cultuur in.

Klik op Verzenden.

Klik op Opslaan.

Taalvarianten van de eigenschapseditor toestaan
Cultuur en hostnamen toevoegen aan het hoofdknooppunt van de website
Volg deze stappen om cultuur en hostnamen toe te voegen:

Ga naar het gedeelte Inhoud.

Klik op de ... stippen naast het knooppunt Inhoud Startpagina.

Selecteer Cultuur en Hostnamen.

Voeg een domein toe voor elke hostnaam, zoals hier is gedaan:

Klik op Opslaan.

Cultuur en Hostnamen
Taalvarianten toevoegen aan de inhoud
U vindt een taaldropdown boven uw inhoudsboom. Als deze er niet is, moet u de pagina mogelijk vernieuwen:

Taal van inhoudsboom
In de taaldropdown vindt u alle talen die u voor uw site hebt geïnstalleerd. U kunt ertussen schakelen om de inhoudsvariaties voor elke taal bij te werken.

Volg deze stappen om taalvarianten toe te voegen aan de inhoud:

Ga naar het knooppunt Home Page. U vindt een taaldropdown naast de titel bovenaan.

Taalvariantdropdown
Klik op de dropdown. U ziet een optie Split view naast de nieuwe taal.

Open taal in Splitview
Klik op Split view. We kunnen nu het inhoudsknooppunt met elke taal naast elkaar zien.

U ziet misschien dat de hoofdtekst grijs is - dit komt omdat we het selectievakje Variatie per cultuur niet hebben aangevinkt.

Splitview-bewerking
Voer de naam in voor uw contentknooppunt en de paginatitel in de nieuwe taal.

Klik op Opslaan en publiceren.

Het venster Klaar om te publiceren wordt geopend en biedt de optie om in een of meer talen te publiceren.

Variantinhoud publiceren
U kunt een of meerdere talen selecteren en op Opslaan en publiceren klikken.

De taalvariant in de browser bekijken
Volg deze stappen om de taalvariant in de browser te bekijken:

Ga naar het gedeelte Inhoud.

Selecteer uw nieuwe taal in de vervolgkeuzelijst Taal boven uw contentboom.

Selecteer het knooppunt Startpagina en ga naar het tabblad Info.

U ziet de links met het nieuwe taaldomein eraan toegevoegd. Als het er niet is, moet u de pagina mogelijk vernieuwen.

De koppeling Taalvariant bekijken
Klik op de link om het nieuwe taalknooppunt in de browser te bekijken.

U kunt de domeinnaam ook toevoegen aan uw localhost in de browser. Bijvoorbeeld: http://localhost:xxxx/da/

Meer informatie

om dit te testen, een login voor deze umbraco-testsite:
gebruiker:admin
e-mail:admin@testing.com
wachtwoord:=XT||C_XGC