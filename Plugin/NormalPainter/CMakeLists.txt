file(GLOB sources *.cpp *.h)
set(plugins_dir "${CMAKE_SOURCE_DIR}/../NormalPainter/Assets/UTJ/NormalPainter/Plugins/x86_64")
add_plugin(NormalPainterCore SOURCES ${sources} PLUGINS_DIR ${plugins_dir})

add_dependencies(NormalPainterCore MeshUtils)
target_link_libraries(NormalPainterCore MeshUtils ${EXTERNAL_LIBS})
install(TARGETS NormalPainterCore DESTINATION .)
