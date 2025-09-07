include($ENV{IDF_PATH}/tools/cmake/version.cmake)

# Déclarer ici les fichiers sources du composant
set(srcs "src/component.cpp")			# indiquer le chemin de nos fichier .cpp sauf le main.cpp

idf_component_register(
		       SRCS ${srcs}
                       INCLUDE_DIRS "include"
                       REQUIRES "driver"          # mettre les dépendances ici = fichiers requis
)
