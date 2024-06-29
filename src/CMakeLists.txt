add_executable(my_project
  main.c
)

target_include_directories(my_project PRIVATE
  ../include
)

target_link_libraries(my_project
  pico_stdlib
  FreeRTOS-Kernel-Heap4
)

set_target_properties(my_project PROPERTIES
  RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}
)

pico_add_extra_outputs(my_project)
