add_library(${PROJECT_NAME} STATIC
        FileHandler.cpp
)

# Namespace-Alias
add_library(FileHandler::FileHandler ALIAS FileHandler)

# Add Include-Path
target_include_directories(FileHandler
        PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/../include>
        PRIVATE
        ${CMAKE_CURRENT_SOURCE_DIR}
)
