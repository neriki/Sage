# Astuce Sage

## Ligne 100

### Restauration d'une base SQL:

* Restaurer la base de données
* Exécuter les commandes:
```SQL
  USE master;
  alter authorization on DATABASE :: [NOM_BDD] to [User Name];

  USE NOM_BDD;
  exec('sp_change_users_login ''update_one'', ''user_cbase'', ''APPL_CBASE''');
```
 
### Déconnexion des utilisateurs:

```SQL  
dbcc cbsqlxp (free);
delete from cbMessage;
delete from cbNotification;
delete from cbRegFile;
delete from cbRegMessage;
delete from cbRegUser;
delete from cbRegMessage;
delete from cbUserSession;
```
  
### Objets métiers:

FactoryDocumentVente.ExistPiece ne va pas regarder dans la colonne dl_piecebl.

Le process IPMEncoder créé automatiquement les lignes d'analytiques, sauf si la propriété bAnalytiqueAuto est mise sur false.

