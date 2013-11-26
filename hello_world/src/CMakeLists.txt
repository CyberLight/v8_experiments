cmake_minimum_required (VERSION 2.6)
project (hello_world)

add_executable (hello_world hello_world.cpp)

include_directories (${v8_root_dir}/include/ /usr/local/include)
TARGET_LINK_LIBRARIES(
	hello_world 
 	${v8_root_dir}/out/x64.release/obj.target/tools/gyp/libv8_base.x64.a
	${v8_root_dir}/out/x64.release/obj.target/tools/gyp/libv8_snapshot.a 
	${v8_root_dir}/out/x64.release/obj.target/third_party/icu/libicui18n.a
	${v8_root_dir}/out/x64.release/obj.target/third_party/icu/libicuuc.a
	${v8_root_dir}/out/x64.release/obj.target/third_party/icu/libicudata.a   
	pthread
)
