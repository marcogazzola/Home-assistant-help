# Backup su Dropbox
*La guida è pensata per il sistema Hassio e prevede l’utilizzo di Add-on esterni.*

1. Aggiungere l'addon **Dropbox Sync** dal repository https://github.com/danielwelch/hassio-dropbox-sync
2. Creare l'app tramite il proprio account di [Dropbox](https://www.dropbox.com/developers/apps) e generare il token
3. Configurare l'addon al punto 1 inserendo il token generato da Dropbox
4. eseguire il sevizio hassio.addon_stdin su Home Assistant
   ```yaml
   - service: hassio.addon_stdin
     data:
       addon: 7be23ff5_dropbox_sync 
       input:
         command: upload
   ```
La guida completa è disponibile [qui](Dropbox-Backup/HomeAssistant-Backup-Dropbox.pdf).

Il package [backupdropbox.yaml](https://github.com/marcogazzola/Home-assistant-help/https://github.com/marcogazzola/Home-assistant-help/Dropbox-Backup/backupdropbox.yaml) contiene un esempio di configurazione completa.