# massa-k-service-bin
Подключение весов Масса-К по http/websocket


## Настройки в appsettings.json:


  "ConnectionStrings": {
  
    "serialPort": "",
    
    "serialResponseL": "20",

    "listenPortTCP": "5001"
    
  }


  serialPort:
  
    - для Wimdows имя порта (COM3 и т.д.), 
    
    - для Linux полный путь к порту /dev/serial/by-id/usb-MASSA-K_MASSA-K_Weight_USB_adapter*******
    


  serialResponseL:
  
    - 20 для весов без передачи веса тары,
    
    - 24 для весов с передачей веса тары.


  listenPortTCP: порт для локального сервиса Websocket


## Получение данных:

Запрос к http сервису:

- запрос: http://localhost:****/GetState

- ответ: {"weightString":"0.017","isStableL":true}

Запрос к Websocket сервису:

- запрос: ws://localhost:****

- ответ: 12|True

