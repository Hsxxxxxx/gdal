add_gdal_driver(TARGET gdal_TileDB SOURCES tiledbdataset.cpp PLUGIN_CAPABLE)
gdal_standard_includes(gdal_TileDB)
target_compile_definitions(gdal_TileDB PRIVATE -DTILEDB_DEPRECATED=)
gdal_target_link_libraries(gdal_TileDB PRIVATE TileDB::tiledb_shared)
