idf_component_register(SRCS "esp32-WOL.c"
                       INCLUDE_DIRS "."
                       PRIV_REQUIRES
                       esp_diagnostics
                       esp_insights
                       esp_system
                       spiffs
                       nvs_flash
                       esp_http_server
                       esp_rainmaker
                       app_network
                       app_insights
                       esp_wifi
)
spiffs_create_partition_image(storage spiffs_image FLASH_IN_PROJECT)
