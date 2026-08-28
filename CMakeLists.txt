set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(PkgConfig REQUIRED)
pkg_check_modules(SODIUM REQUIRED libsodium)

target_link_libraries(your_target PRIVATE sodium)
target_include_directories(your_target PRIVATE ${SODIUM_INCLUDE_DIRS})
# Asio: just #include <asio.hpp> directly — Arch installs headers to /usr/include