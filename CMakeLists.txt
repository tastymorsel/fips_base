#
# project: fips_test/
#
cmake_minimum_required(VERSION 2.8)

# include the fips main cmake file
get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
include("${FIPS_ROOT_DIR}/cmake/fips.cmake")

# include_directories(src)

fips_setup(PROJECT hello)

fips_import_fips_imgui_imgui()
fips_import_fips_lua_lua()
fips_import_fips_libmodplug_libmodplug()

fips_add_subdirectory(src)
# fips_add_subdirectory(src/...)
fips_finish()


