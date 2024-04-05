add_library(boost_system_module)

target_sources(boost_system_module
        PUBLIC
        FILE_SET CXX_MODULES FILES
        module.cpp
)

add_library(boost::module::system ALIAS boost_system_module)

target_link_libraries(boost_system_module PUBLIC Boost::system)