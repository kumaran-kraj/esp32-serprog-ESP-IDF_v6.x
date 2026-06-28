idf_component_register(SRCS "main.c"
                    INCLUDE_DIRS "."
                    REQUIRES esp_driver_spi esp_driver_uart vfs driver esp_netif esp_wifi console)

if(CONFIG_ESP32_SERPROG_WIFI_ENABLED)
    target_sources(${COMPONENT_TARGET} PRIVATE "wifi.c")
endif()
