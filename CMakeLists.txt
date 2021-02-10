cmake_minimum_required(VERSION 2.6)

include(RezBuild)

FILE(GLOB root_files "*.yml" "*.yaml" "*.png" "*.md" "*.qss" "*.py")
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

FILE(GLOB_RECURSE python "python/*")

rez_install_files(
    ${python}
    DESTINATION
    .
    )

FILE(GLOB_RECURSE resources "resources/*")

rez_install_files(
    ${resources}
    DESTINATION
    .
    )
