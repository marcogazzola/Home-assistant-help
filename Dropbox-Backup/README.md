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
La guida completa è disponibile [qui](HomeAssistant-Backup-Dropbox.pdf).

Il package [backupdropbox.yaml](backupdropbox.yaml) contiene un esempio di configurazione completa.

</br>
</br>
<style>.bmc-button img{width: 27px !important;margin-bottom: 1px !important;box-shadow: none !important;border: none !important;vertical-align: middle !important;}.bmc-button{line-height: 36px !important;height:37px !important;text-decoration: none !important;display:inline-flex !important;color:#FFFFFF !important;background-color:#FF813F !important;border-radius: 3px !important;border: 1px solid transparent !important;padding: 1px 9px !important;font-size: 22px !important;letter-spacing: 0.6px !important;box-shadow: 0px 1px 2px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;margin: 0 auto !important;font-family:'Cookie', cursive !important;-webkit-box-sizing: border-box !important;box-sizing: border-box !important;-o-transition: 0.3s all linear !important;-webkit-transition: 0.3s all linear !important;-moz-transition: 0.3s all linear !important;-ms-transition: 0.3s all linear !important;transition: 0.3s all linear !important;}.bmc-button:hover, .bmc-button:active, .bmc-button:focus {-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;text-decoration: none !important;box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;opacity: 0.85 !important;color:#FFFFFF !important;}</style><link href="https://fonts.googleapis.com/css?family=Cookie" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/Gazzolinho"><img src="https://www.buymeacoffee.com/assets/img/BMC-btn-logo.svg" alt="Buy me a beer"><span style="margin-left:5px">Buy me a beer</span></a>