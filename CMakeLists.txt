zephyr_library()

if ((NOT CONFIG_ZMK_SPLIT) OR CONFIG_ZMK_SPLIT_ROLE_CENTRAL)
  zephyr_library_sources_ifdef(CONFIG_ZMK_BEHAVIOR_NON_OVERLAP src/behaviors/behavior_non_overlap.c)
  zephyr_include_directories(${APPLICATION_SOURCE_DIR}/include)
endif()
