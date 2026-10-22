## Explicació
Per fer el diagrama mermaid primer fem les taules posen el nombre de la taula i omplin els seus valors dintre de `{ }` podem definir valors posen el seu nom amb el seu tipus com els següents:

```
string	Text
char	Un sol caràcter
boolean / bool	verdader o fals
int / integer	Nombre enter
```
Aquí estan els tipus de relació que poden tenir les taules entre eelles podem tenir les següents possibilitats depenen del tipus de comportament que poden tenir entre elles com per exemple `||--|| : acció o fet` com per exemple un personatge pot acompanyar una mascota_

>   |o : Un o zero
>
>    || : Exactament un
>
>    }o : Molts o zero
>
>   }| : Molts o un
>
>    o| : Zero o un

També per resoldre els dubtes o problemes que vaig tenir fent el diagrama vaig utilitzar la documentació oficial de **[mermaid](https://mermaid_ai/open-source/syntax/entityRelationshipDiagram_html)**_

```mermaid
---
title: Model Conceptual
config:
    layout: dagre
---
erDiagram
PERSONATGE ||--||MASCOTA : ACOMPANYA
PERSONATGE }o--o{ HABILITAT: POSEEIX
PERSONATGE }o--o{ ITEM: EQUIPA
PERSONATGE }o--o{ ENEMIC: ENFRENTA
ENEMIC }o--o{ HABILITAT: POSEEIX
HABILITAT }o--o{ HABILITAT: COMBINA
MASCOTA ||--o{ ITEM: CARREGA
        HABILITAT {
                int CODI PK
                string NOM "NOT NULL"
                string tipus "NOT NULL"
                int COST
                int DANY
                int COOLDOWN
        }
     PERSONATGE {
                STRING DNI PK
                string NOM "NOT NULL"
                string COGNOM
                int FORÇA
                int VIDA
                int AGILITAT
                int CARISMA
        }
     ITEM {
                int CODI PK
                string NOM "NOT NULL"
                bool EQUIPABLE
                bool COMERCIABLE "NOT NULL"
                string tipus "NOT NULL"
                int PES "NOT NULL"
                int QUALITAT "NOT NULL"
                float MESURES_X "NOT NULL"
                float MESURES_Y "NOT NULL"
                float MESURES_Z "NOT NULL"
        }
   MASCOTA {
                int NUM_CHIP PK
                string NOM "NOT NULL"
                string MOTXILLA
        }
  ENEMIC {
                int CODI PK
                string NOM "NOT NULL"
                string TIPUS "NOT NULL"
                int NIVELL "NOT NULL"
                int VIDA
                int FORÇA
                int AGILITAT
                int CARISMA
        }
``` 
