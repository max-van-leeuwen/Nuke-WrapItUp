cmake_minimum_required(VERSION 2.8)

include(RezBuild)

file(GLOB python_files "WrapItUp/*.py")
rez_install_files(
    ${python_files}
    DESTINATION .
)
