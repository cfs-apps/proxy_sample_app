project(CFE_SAMPLE_APP C)
# This file is from https://github.com/cfs-apps/proxy_sample_app

include_directories(fsw/mission_inc)
include_directories(fsw/platform_inc)
include_directories(fsw/src)
include_directories(${sample_lib_MISSION_DIR}/fsw/public_inc)

aux_source_directory(fsw/src APP_SRC_FILES)
aux_source_directory(fsw/tables APP_TABLE_FILES)

# Create the app module
add_cfe_app(sample_app ${APP_SRC_FILES})
add_cfe_tables(sample_app ${APP_TABLE_FILES})

