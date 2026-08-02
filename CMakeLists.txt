# MQ2Clipboard
# Forked from RedGuides/MQ2Clipboard (github.com/RedGuides org sweep, forum-plugins-2026-08-02
# follow-up batch). Vendored as a git submodule tracking https://github.com/blbruegg/MQ2Clipboard
# (fork of RedGuides/MQ2Clipboard). See F:\\EQProject\\docs\\re_progress.md for the write-up.

include("../../Plugin.cmake")

set(MQ2Clipboard_SOURCES
    "MQ2Clipboard.cpp"
    "MQ2Clipboard.rc"
    "resource.h"
)

source_groups("Source Files" ${MQ2Clipboard_SOURCES})

add_library(MQ2Clipboard SHARED
    ${MQ2Clipboard_SOURCES}
)

set_target_properties(MQ2Clipboard PROPERTIES FOLDER "core/plugins")

target_Plugin_props(MQ2Clipboard)

target_link_libraries(MQ2Clipboard PRIVATE MQ2Main)
