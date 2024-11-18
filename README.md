# Gruppexamination: Take Away-restaurangen

## Inledning

*“Välkommen till vårt kreativa kök!”*

Tänk er det här: ni har precis fått ett samtal från ett spännande nystartat företag som har en vision om att revolutionera take away-marknaden för restauranger. De är trötta på det gamla vanliga, och nu vill de slå på stort – och det är här ni kommer in i bilden! Er uppgift? Skapa ett grymt koncept som får kunderna att trycka på “beställ” innan de ens hunnit blinka!

Ni kommer att ansvara för att bygga hela varumärket från grunden. Det innebär att ni hittar på ett namn som folk kommer att minnas, en visuell identitet som gör att restaurangen står ut i mängden, och en webbsida där kunder enkelt kan beställa sina favoriträtter. Men inte nog med det! På insidan behöver restaurangen ett smidigt system där de anställda kan hantera menyn, ordrar och allt annat som gör att matlagningen kan rulla på utan krångel.

Det här är er chans att kombinera era talanger inom kreativt tänkande, webbdesign och systemutveckling – och självklart att ha kul medan ni gör det!

## Specifikation

Som ert examinerande fullstackprojekt skall ni bygga en webbsida för en restaurang som uteslutande erbjuder take away-servering.

Ni bestämmer själva restaurangens namn, tema, grafiska profil, samt vilken sorts mat och dryck som serveras. 

Restaurangens kunder skall kunna använda webbsidan för att:
* Läsa menyn
* Göra en take away-beställning
* Ändra eller ångra en lagd beställinng (innan den är låst av personalen)
* Få information om restaurangen

Restaurangens anställda skall kunna använda webbsidan för att:
* Se inlagda beställningar
* Se vilka beställningar som ännu inte behandlats
* Låsa en beställning när den skickas till köket så att den inte kan ändras eller ångras
* Ändra detaljer i en beställning
* Lägga med en kommentar i bestälningen (till kocken)

Ni har alltså två olika sorters användare: **kunder** och **anställda**. Kom ihåg att dessa två användargrupper har olika behov! Ni hittar User Stories för projektet längre ner under rubriken **Länkar**. Antingen behåller ni dessa som de är, eller så bryter ni ner dem i mindre "tasks" när ni tar in de i er Sprint Backlog.
Tänk på att detta projekt kan användas för att söka LIA eller jobb i framtiden, så se till att lägga ner ett ordentligt arbete!

## Innehåll

Detta projekt kommer kombinera allt som ni har lärt er i utbildningen hittills:
* Arbeta agilt enligt Scrum
* Designprocessen
* Git och GitHub
* HTML & CSS, responsiv design
* React
* AWS serverless framework / Express.js
* AWS S3 bucket

### Scrum

Ni ska följa Scrum-metoden till punkt och pricka genom hela utvecklingsprocessen. Detta innebär **sprint planning**, **daily scrum** varje dag ni arbetar med projektet, **sprint review** och **sprint retrospective** som sker på måndagar och fredagar respektive. En sprint är 1 vecka lång.

## User stories

User stories hittar ni här: https://github.com/users/zocom-christoffer-wallenberg/projects/16/views/1

### Designprocessen

Ni har Design Thinking-modellen till ert förfogande, MEN för att komma igång snabbt så behöver den inte genomföras till punkt och pricka. Här fokuserar ni inledningsvis på ert koncept, kom på ett riktigt kickass-namn åt er restaurang och börja designa i Figma. Se till att ni prototyper alla era vyer och diskutera i teamet så att ni är överens och alla är med på slutresultatet.

### Git och GitHub

Ni får själva välja om ni vill köra ett s.k. monorepo innehållandes både er frontend och er backend, eller om ni vill skapa upp separata repon. Därefter skapar ni upp ett (1) projekt på GitHub Projects som ni kopplar ihop med båda ert/era repo(n). Er "board" kommer att vara en "single source of truth" under projektets gång. Det är här ni lägger in alla era user stories, samt specificerar EXAKT vad som behöver göras för att lösa en user story / issue. Er "board" bör minst innehålla följande kategorier: *Product Backlog*, *Sprint Backlog*, *In progress*, *Done*, men ni får även lägga till fler exempelvis *test*, *On hold* etc. Även om man slutfört sina uppgifter/issues så kommer jag att räkna arbetet som "ej slutfört" om man inte aktivt uppdaterar sin "board" allt eftersom arbetet fortskrider. Jag kommer kika in lite då och då för att anteckna hur flitigt ni arbetar och ta med detta i min slutliga bedömning.

Ni behöver bjuda in mig till både era repon och ert projekt (zocom-christoffer-wallenberg) om dessa är privata. **Jag vill ha tillgång till era repon och er board från och med denna vecka.**

### Frontend

Appens frontend ska byggas i React och Typescript. Planera projektet så att ni åtminstonde kan börja koda er frontend innan ni har en fullt fungerande backend. Ni kan komma att behöva skapa realistisk testdata att använda tills vidare, och till detta är Aizo en utmärkt medhjälpare. 

Er webbsida måste även vara responsiv och fungera på ALLA skärmar.

### Backend

Här ställs ni inför ett par avvägningar. Antingen så bygger ni er backend i Express.js, eller så bygger ni den serverless i AWS.
Oavsett vilket ni väljer så finns det vissa saker ni MÅSTE använda er utav.

* Hantering av credentials på ett säkert sätt (JWT, sessions, cookies) (Detta kommer vi gå igenom)
* En API-nyckel som skall skickas med i alla anrop
* Middlewares för att autentisera, validera osv.
* En databas för persistent datalagring
* En Content Security Policy (Detta kommer vi gå igenom)
* Hosta er backend någonstans

#### Express - utmaningen

Dels kommer ni att behöva lära er hur man hostar sin beckend på Render, men den stora utmaningen tänker jag kan bli databashanteringen. NeDB har inget grafiskt gränssnitt vilket underlättar vi databasimplementation, och jag tänker att en bra idé här kan vara en idé att sätter er in i MongoDB som är supersmidigt och har ett lättuggat gränssnitt. **Dock går det bra med att använda NeDB också för denna examination**.

Guide till Render: https://www.youtube.com/watch?v=bnCOyGaSe84

#### Serverless i AWS

Dels så kommer ni återigen vara tvugna att samarbeta i serverless framework med allt som det medför, bestämmande av vems backend man kommer använda i slutändan osv. Den stora utmaningen här blir dock hur ni gör för att trycka in middlewares i er applikation. Ett verktyg ni isåfall kommer behöva använda er av är Middy (jag kommer demonstrera detta under vecka 1).

### AWS S3

Appen skall publiceras online med AWS i en S3 bucket inför varje Sprint Review.

## Inlämning, slutredovisning och bedömning

Deadline för ert projektarbete är **fredagen den 13/12 kl 23:59**. I er inlämning vill jag ha länkar till era Github-repon, ert projekt, samt ert Figma-projekt (se också för guds skull till att jag har tillgång till allt detta, jag kommer inte jaga er under jul och nyår och kommer jag inte in så kan det inte bli godkänt). 

Även om det är ett grupprojekt så är det individuella betyg som gäller. 

**För G krävs att ni har**:
* Byggt en applikation som innehåller all funktionalitet som specificeras under Specifikationer
* Byggt er applikation i React och TypeScript med en backend
* Använder sig av en Content Security Policy i ert projekt
* Använder sig av JWT (cookies, session storage eller local storage)

**För VG krävs att ni**
* Har använt en genomtänkt arkitektur i ert React-projekt och använder `intermediate` eller ´advanced folder structure´ från artikeln som ni hittar [här](https://blog.webdevsimplified.com/2022-07/react-folder-structure/).

Kom gärna överens som grupp vilket betyg ni vill satsa på, och arbeta tillsammans utefter det. Hamnar man i en grupp som satsar mot G men att man själv vill uppnå ett VG, så kan man kontakta mig så tittar vi på vad du som individ behöver göra för att nå det högre betyget.

Projektet skall presenteras för klassen fredagen den 13 december. Projektet ska presenteras och demonstreras på engelska då detta är ett av kursmålen.
Mer info om upplägg kring detta kommer senare.

Lycka till!
