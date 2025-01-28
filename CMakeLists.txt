#Finding GTK3 file 

find_package(PkConfig REQUIRED)
pkg_check_modules(GTK3 REQUIRED gtk+-3.0)

#Including directories and link the libraries 

include_directories(${GTK3_INCLUDE_DIRS})
link_directories(${GTK3_LIBRARY_DIRS})
add_definitions(${GTK3_CFLAGS_OTHER})

#Add Excecutable 
add_executable(AriBrowser main.ccp)
target_link_libraries(AriBrowser ${GTK3_LIBRARIES})