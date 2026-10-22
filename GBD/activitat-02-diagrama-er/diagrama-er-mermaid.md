

```mermaid
erDiagram
        HABILITAT {
                int CODI PK
                string NOM "NOT NULL"
                string tipus "NOT NULL"
                int COST
                int DANY
                int COOLDOWN
        }
     PRSONATGE {
                int DNI PK
                string NOM "NOT NULL"
                string COGNOM
                int FORÇA
                int VIDA
                int AGILITAT
                int CARISMA
        }
``` 
