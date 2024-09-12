Som en overordnet reflektion, efter færdiggørrelsen af sitet, synes jeg, at det har været meget ligetil, og rimeligt nemt at forstå.
De udfordringer, jeg har haft, har primært været I forbindelse med, at vi jo ikke har haft designerene, at tage fat på og stille spørgsmål til. Der har bla. været nogle uoverensstemmelser ifm med farver, størrelser og spacing både fra side til side, eller sektion til sektion, men også mellem details siden og det resterende site.

Specifikt har jeg forsøgt at implementere vores nylærte metoder, hvor jeg følte det var passende. Jeg ville herefter sagtens kunne gå ind, og yderligere optimere koden. De forsøg jeg har foretaget mig ifm metoderne, har udelukkende været efterhånden, som jeg har skrevet koden.

Generelt, har jeg de fleste steder brugt nesting. Dette vil jeg ikke give et konkret eksepel på, da dette også kan ses i mine andre eksempler.

Jeg har gjort brug af utopia til at udvikle størrelser til fonte og spacing. Disse har jeg sat ind som variabler øverst i global.css, og det er hovedsageligt disse variabler, jeg har brugt til enhver størrelse, hele sitet igennem.

Et eksemplet kan ses her, ved min button. Her har jeg gjort burg af de genererede størrelser. Jeg har desuden gjort brug af yderligere variabel-navne, for nemmere at kunne referere senere hen.

    button {
        place-self: end;

        color: var(--button-color, var(--secondary-2));
        background: var(--button, var(--primary-3));
        border: solid 0.125rem var(--primary-3);
        &:hover {
            --button: var(--secondary-2);
            --button-color: var(--primary-3);
        }
        &:active {
            --button: oklch(from var(--primary-3) calc(l + 0.15) c h);
        }
    }

I mit newsletter komponent, har jeg desuden gjort burg af container queries, til at gøre newsletteret responsivt. Jeg har dog primært til andre komponenter / sider gjort brug af media queries, da jeg havde lidt problemer med containers, og hvordan de påvirkede indholdet.

    @container (width <= 878px) {
        p {
            max-width: 100%;
        }
        input {
            padding-right: var(--space-l-4xl);
        }
    }
    @container (width > 878px) {
        input {
            padding-right: var(--space-4xl);
        }
    }

Overordnet, vil jeg dog se projektet som en succes. Jeg har forbedret mine egne færdigheder specielt i forbindelse med css, og trods der stadig er plads til forbedringer, er jeg landet et sted, hvor jeg selv føler, at jeg har opnået alt, hvad jeg havde håbet på.
