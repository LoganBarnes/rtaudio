include_directories(..)
if (WIN32)
    include_directories(../include)
endif (WIN32)

add_executable(audioprobe audioprobe.cpp)
target_link_libraries(audioprobe rtaudio_static)

add_executable(playsaw playsaw.cpp)
target_link_libraries(playsaw rtaudio_static)

add_executable(playraw playraw.cpp)
target_link_libraries(playraw rtaudio_static)

add_executable(record record.cpp)
target_link_libraries(record rtaudio_static)

add_executable(duplex duplex.cpp)
target_link_libraries(duplex rtaudio_static)

if (UNIX) # temporary until implemented for windows
    add_executable(testcallbackonly testcallbackonly.cpp)
    target_link_libraries(testcallbackonly rtaudio_static)
endif ()

add_executable(testall testall.cpp)
target_link_libraries(testall rtaudio_static)

add_executable(teststops teststops.cpp)
target_link_libraries(teststops rtaudio_static)
