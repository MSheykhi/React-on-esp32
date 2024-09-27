idf_component_register(
  SRCS 
    "routes/pushBtn.c"
    "routes/toggleLed.c"
    "routes/helloWorld.c"
    "routes/servo.c"
    "main.c"
  INCLUDE_DIRS 
    "."
    "routes"
  REQUIRES esp_netif json esp_http_server driver wifi nvs_flash spiffs
  )

spiffs_create_partition_image(spiffs ../site/dist FLASH_IN_PROJECT)                    