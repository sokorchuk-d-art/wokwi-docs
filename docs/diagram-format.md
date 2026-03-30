{
  "version": 1,
  "author": "Sergiy",
  "editor": "wokwi",
  "parts": [
    { "type": "board-esp32-devkit-c-v4", "id": "esp", "top": 0, "left": 0, "attrs": {} },
    { "type": "wokwi-potentiometer", "id": "moisture_sensor", "top": -80, "left": 200, "attrs": { "label": "Датчик вологості" } },
    { "type": "wokwi-led", "id": "led_tx", "top": 50, "left": 200, "attrs": { "color": "blue", "label": "Імітація передачі LoRa" } }
  ],
  "connections": [
    [ "esp:3V3", "moisture_sensor:VCC", "red", [ "v-20" ] ],
    [ "esp:GND.1", "moisture_sensor:GND", "black", [ "v-40" ] ],
    [ "esp:34", "moisture_sensor:SIG", "green", [ "v0" ] ],
    [ "esp:GND.2", "led_tx:C", "black", [ "v0" ] ],
    [ "esp:2", "led_tx:A", "blue", [ "v0" ] ]
  ],
  "dependencies": {}
}
