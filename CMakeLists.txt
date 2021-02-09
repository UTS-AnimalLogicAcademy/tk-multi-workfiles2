cmake_minimum_required(VERSION 2.6)

include(RezBuild)

FILE(GLOB root_files "*.yml" "*.yaml" "*.png" "*.md" "*.qss")
rez_install_files(
    ${root_files}
    DESTINATION
    .
)

FILE(GLOB_RECURSE hooks "hooks/*")

rez_install_files(
    ${hooks}
    DESTINATION
    .
    )
