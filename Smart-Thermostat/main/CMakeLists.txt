set(COMPONENT_SRCS "main.c" "ui.c" "fft.c" "wifi.c")
set(COMPONENT_ADD_INCLUDEDIRS "." "./includes")
set(COMPONENT_REQUIRES "nvs_flash" "esp-aws-iot" "esp-cryptoauthlib" "Core2ForAWS" "json")
register_component()

target_add_binary_data(${COMPONENT_TARGET} "certs/aws-root-ca.pem" TEXT)