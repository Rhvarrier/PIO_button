pico_generate_pio_header(pio_button_debounce ${CMAKE_CURRENT_LIST_DIR}/button_debounce.pio)

add_library(button_debounce PRIVATE button_debounce.cpp)

target_link_libraries(button_debounce PRIVATE
        pico_stdlib
        hardware_pio
        )
target_include_directories(button_debounce PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

