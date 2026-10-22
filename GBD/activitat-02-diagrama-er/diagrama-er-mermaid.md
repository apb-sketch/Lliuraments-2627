

```mermaid
erDiagram
PERSONATGE ||-||MASCOTA : ACOMPANYA
        HABILITAT {
                int CODI PK
                string NOM "NOT NULL"
                string tipus "NOT NULL"
                int COST
                int DANY
                int COOLDOWN
        }
     PERSONATGE {
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
   MASCOTA {
                int NUM.CHIP PK
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
