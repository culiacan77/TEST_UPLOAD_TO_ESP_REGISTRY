include($ENV{IDF_PATH}/tools/cmake/version.cmake)

set(srcs "src/component.cpp")     #mettre le contenu du dossier src

idf_component_register(SRCS ${srcs}
                       INCLUDE_DIRS "include"
                       REQUIRES "driver"           #mettre ici ce dont on a besoin ex "leg strip"
)
