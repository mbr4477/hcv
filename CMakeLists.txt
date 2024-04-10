cmake_minimum_required(VERSION 3.5)
project(HCV C)

add_subdirectory(cfe)

add_custom_target(tables-staging COMMAND mkdir -p ${MISSION_BINARY_DIR}/tables/staging)
add_dependencies(mission-install tables-staging)