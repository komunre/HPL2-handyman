cmake_minimum_required (VERSION 2.8.11)
project(Launcher)

FindPrebuiltLibrary(FLTK_LIBRARY fltk)
FindPrebuiltLibrary(FLTK_IMAGES_LIBRARY fltk_images)
FindPrebuiltLibrary(JPEG_LIBRARY jpeg)

find_package(X11)

add_executable(Launcher
    launcher.cpp
    Main.cpp
    QualityChooser.cpp
    LauncherHelper.cpp)
target_link_libraries(Launcher HPL2 ${FLTK_IMAGES_LIBRARY} ${FLTK_LIBRARY} Xext Xft fontconfig ${JPEG_LIBRARY} ${X11_Xrender_LIB} ${X11_Xcursor_LIB} ${X11_Xfixes_LIB} ${X11_Xext_LIB} ${X11_Xft_LIB} ${X11_Xinerama_LIB} ${X11_LIBRARIES})

# vim: et ts=4
