cmake_minimum_required(VERSION 3.6 FATAL_ERROR)

project(WebScrape VERSION 0.1.0)

# zlib-1.2.11
include_directories(dependencies/zlib-1.2.11/include)
link_directories(dependencies/zlib-1.2.11/lib)

# libcurl-vc-x86-release-static-ipv6-sspi-winssl
include_directories(dependencies/libcurl-vc-x86-release-static-ipv6-sspi-winssl/include)
link_directories(dependencies/libcurl-vc-x86-release-static-ipv6-sspi-winssl/lib)

add_executable(Main main.cpp)
set_property(DIRECTORY PROPERTY VS_STARTUP_PROJECT Main)
add_definitions(-DCURL_STATICLIB)

target_link_libraries(Main zlibstatic libcurl_a Ws2_32.lib Wldap32.lib crypt32.lib normaliz.lib)
