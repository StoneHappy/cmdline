set(TARGET_NAME cmdline_test1)

add_executable(${TARGET_NAME} main.cpp)

target_compile_options(${TARGET_NAME} PUBLIC "$<$<COMPILE_LANG_AND_ID:CXX,MSVC>:/WX->")

target_link_libraries(${TARGET_NAME}
          cmdline
)