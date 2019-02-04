# Package per l'integrazione di Xiaomi Vacuum in Home Assistant

1. Per configurare correttamente il [package](pkg_vacuum_xiaomi.yaml) inserire le seguenti voci nel file `secrets.yaml`

  **Sostituire l'IP indicato con l'indirizzo del proprio vacuum**
```yaml
xiaomi_vacuum_ip: 192.168.1.132
xiaomi_vacuum_token: xxxxxxxxxxxxxxxxxxxx #Token precedentemente ricavato da Mi Home
xiaomi_vacuum_resource_map: http://192.168.1.132/api/remote/map
```
2. Copiare le immagini presenti nella cartella [image](image/) nella cartella /config/www/image di Home Assistant
3. Copiare il file [entity-attributes-card.js](entity-attributes-card.js) nella cartella /config/www di Home Assistant
4. Per visualizzare una scheda personalizzata in lovelace, utilizzare il [seguente codice](ui-lovelace.yaml) integrandolo nel proprio file ui-lovelace.yaml. 
**[importante avere attiva la modalità yaml di lovelace!!](https://www.home-assistant.io/lovelace/yaml-mode/)**
5. Per utilizzare la pulizia a zone _ottimizzata_ installare il custom_component presente [qui](https://github.com/home-assistant/home-assistant/pull/19777) finche la Pull request non verrà approvata.


## Il risultato dovrebbe essere questo:

<div style="text-align:center"><img src="guida/vacuum_lovelace.jpg" width="40%"></div>

</br>
</br>
<style>.bmc-button img{width: 27px !important;margin-bottom: 1px !important;box-shadow: none !important;border: none !important;vertical-align: middle !important;}.bmc-button{line-height: 36px !important;height:37px !important;text-decoration: none !important;display:inline-flex !important;color:#FFFFFF !important;background-color:#FF813F !important;border-radius: 3px !important;border: 1px solid transparent !important;padding: 1px 9px !important;font-size: 22px !important;letter-spacing: 0.6px !important;box-shadow: 0px 1px 2px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;margin: 0 auto !important;font-family:'Cookie', cursive !important;-webkit-box-sizing: border-box !important;box-sizing: border-box !important;-o-transition: 0.3s all linear !important;-webkit-transition: 0.3s all linear !important;-moz-transition: 0.3s all linear !important;-ms-transition: 0.3s all linear !important;transition: 0.3s all linear !important;}.bmc-button:hover, .bmc-button:active, .bmc-button:focus {-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;text-decoration: none !important;box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;opacity: 0.85 !important;color:#FFFFFF !important;}</style><link href="https://fonts.googleapis.com/css?family=Cookie" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/Gazzolinho"><img src="https://www.buymeacoffee.com/assets/img/BMC-btn-logo.svg" alt="Buy me a beer"><span style="margin-left:5px">Buy me a beer</span></a>