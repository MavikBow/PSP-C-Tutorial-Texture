cmake_minimum_required(VERSION 3.0)

project(Triangle_Sample)

add_executable(${PROJECT_NAME} main.c)

target_link_libraries(${PROJECT_NAME} PRIVATE
    pspdisplay
    pspgu
    pspgum
    pspkernel
    pspdebug
    pspge
    pspvramalloc
)

# Create an EBOOT.PBP file
create_pbp_file(
    TARGET ${PROJECT_NAME}
    ICON_PATH NULL
    BACKGROUND_PATH NULL
    PREVIEW_PATH NULL
    TITLE ${PROJECT_NAME}
)