add_executable(sample-unzip src/unzip.cpp)
if(WINCE)
	set_target_properties(sample-unzip PROPERTIES LINK_FLAGS "/ENTRY:wmainCRTStartup")
endif()
target_link_libraries(sample-unzip PUBLIC Poco::Zip Poco::Util Poco::XML)
