set(COMPONENT_SRCDIRS "src")

if(${BOOTLOADER_BUILD})
    set(COMPONENT_ADD_INCLUDEDIRS "include include_priv")
    set(COMPONENT_REQUIRES)
    set(COMPONENT_PRIV_REQUIRES spi_flash)
else()
    set(COMPONENT_ADD_INCLUDEDIRS "include")
    set(COMPONENT_PRIV_INCLUDEDIRS "include_priv")
    set(COMPONENT_REQUIRES)
    set(COMPONENT_PRIV_REQUIRES spi_flash mbedtls)
endif()

register_component()
