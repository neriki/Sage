# Astuce Sage

## Ligne 100

### Restauration d'une base SQL:

* Restaurer la base de données
* Exécuter les commandes:
```SQL
  USE master;
  alter authorization on DATABASE :: [NOM_BDD] to [User Name];
```

```SQL
  USE NOM_BDD;
  sp_change_users_login 'update_one', 'user_cbase', 'APPL_CBASE'
```
  
### Objets métiers:

FactoryDocumentVente.ExistPiece ne va pas regarder dans la colonne dl_piecebl.

