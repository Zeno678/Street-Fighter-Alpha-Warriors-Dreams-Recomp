# Distributed under the OSI-approved BSD 3-Clause License.  See accompanying
# file Copyright.txt or https://cmake.org/licensing for details.

cmake_minimum_required(VERSION 3.31.12)

# Reject any attempt to use a toolchain file. We must not use one because
# we could be downloading it here. If the CMAKE_TOOLCHAIN_FILE environment
# variable is set, the cache variable will have been initialized from it.
unset(CMAKE_TOOLCHAIN_FILE CACHE)
unset(ENV{CMAKE_TOOLCHAIN_FILE})

# We name the project and the target for the ExternalProject_Add() call
# to something that will highlight to the user what we are working on if
# something goes wrong and an error message is produced.

project(libjuice-populate NONE)



include(ExternalProject)
ExternalProject_Add(libjuice-populate
                     "UPDATE_DISCONNECTED" "False" "DOWNLOAD_EXTRACT_TIMESTAMP" "TRUE" "EXTERNALPROJECT_INTERNAL_ARGUMENT_SEPARATOR" "URL" "https://github.com/paullouisageneau/libjuice/archive/refs/tags/v1.7.2.tar.gz" "URL_HASH" "SHA256=75159867c4a5a689a6559e11aa0d30c9eba12ce73a4ae3d898b521467e1f635d"
                    SOURCE_DIR          "/var/home/dodo/Street-Fighter-Alpha-Warriors-Dreams-Recomp/build-release/_deps/libjuice-src"
                    BINARY_DIR          "/var/home/dodo/Street-Fighter-Alpha-Warriors-Dreams-Recomp/build-release/_deps/libjuice-build"
                    CONFIGURE_COMMAND   ""
                    BUILD_COMMAND       ""
                    INSTALL_COMMAND     ""
                    TEST_COMMAND        ""
                    USES_TERMINAL_DOWNLOAD  YES
                    USES_TERMINAL_UPDATE    YES
                    USES_TERMINAL_PATCH     YES
)


