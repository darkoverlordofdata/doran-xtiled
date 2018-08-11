cmake_minimum_required ( VERSION 3.1 )
###################################################################################
#
#   Library: xtiled
#
###################################################################################
project ( xtiled VERSION 0.0.1 )

# Includes: 

# C Sources: 

# Vala Sources: 
list ( APPEND SOURCE .lib/xtiled/src/LayerList.vala )
list ( APPEND SOURCE .lib/xtiled/src/Map.vala )
list ( APPEND SOURCE .lib/xtiled/src/Line.vala )
list ( APPEND SOURCE .lib/xtiled/src/MapObject.vala )
list ( APPEND SOURCE .lib/xtiled/src/MapReader.vala )
list ( APPEND SOURCE .lib/xtiled/src/ObjectLayer.vala )
list ( APPEND SOURCE .lib/xtiled/src/Polygon.vala )
list ( APPEND SOURCE .lib/xtiled/src/Polyline.vala )
list ( APPEND SOURCE .lib/xtiled/src/Tile.vala )
list ( APPEND SOURCE .lib/xtiled/src/TileData.vala )
list ( APPEND SOURCE .lib/xtiled/src/Property.vala )
list ( APPEND SOURCE .lib/xtiled/src/Tileset.vala )
list ( APPEND SOURCE .lib/xtiled/src/TileLayer.vala )
list ( APPEND SOURCE .lib/xtiled/src/xtiled.vala )

# Vapis: 

# Vapidir: 
list ( APPEND VALA_OPTION --vapidir=${CMAKE_SOURCE_DIR}/.lib/xtiled/vapis)

## Export to the parent scope:
set ( XTILED true PARENT_SCOPE )


set ( VALA_SOURCES "${VALA_SOURCES};${SOURCE}" PARENT_SCOPE )

set ( VALAC_OPTIONS "${VALAC_OPTIONS};${VALA_OPTION}" PARENT_SCOPE )
set ( DEPS_LIBRARIES "${DEPS_LIBRARIES};-lm" PARENT_SCOPE)


# (generated from template: package. Do not modify. )
