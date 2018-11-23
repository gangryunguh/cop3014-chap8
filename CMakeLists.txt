cmake_minimum_required(VERSION 3.10)
project(chap8)

set(CMAKE_CXX_STANDARD 11)
set(SOURCE_FILES app/Pr8-1.cpp app/Pr8-2.cpp app/Pr8-3.cpp
        app/Pr8-4.cpp app/Pr8-5.cpp app/Pr8-6.cpp
        app/Pr8-7.cpp app/Pr8-8.cpp app/Pr8-9.cpp)

add_executable(Pr8-1.exe app/Pr8-1.cpp )
add_executable(Pr8-2.exe app/Pr8-2.cpp)
add_executable(Pr8-3.exe app/Pr8-3.cpp)
add_executable(Pr8-4.exe app/Pr8-4.cpp)
add_executable(Pr8-5.exe app/Pr8-5.cpp)
add_executable(Pr8-6.exe app/Pr8-6.cpp)
add_executable(Pr8-7.exe app/Pr8-7.cpp)
add_executable(Pr8-8.exe app/Pr8-8.cpp)

if (WIN32)
    set(SFML_STATIC_LIBRARIES TRUE)
endif()

set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake_modules")
find_package(SFML REQUIRED COMPONENTS audio graphics window system)

#if (SFML_FOUND)
#    include_directories(${SFML_INCLUDE_DIR})
#    if (WIN32)
#        target_link_libraries(draw_sin.exe ${SFML_LIBRARIES} ${SFML_DEPENDENCIES})
#        target_link_libraries(draw_map.exe ${SFML_LIBRARIES} ${SFML_DEPENDENCIES})
#    else()
#        target_link_libraries(draw_sin.exe ${SFML_LIBRARIES})
#        target_link_libraries(draw_map.exe ${SFML_LIBRARIES})
#    endif()
#endif()
