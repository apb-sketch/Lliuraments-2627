

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
     ITEM {
                int CODI PK
                string NOM "NOT NULL"
                bool EQUIPABLE
                bool COMERCIABLE "NOT NULL"
                string tipus "NOT NULL"
                int PES "NOT NULL"
                int QUALITAT "NOT NULL"
        }
``` 
