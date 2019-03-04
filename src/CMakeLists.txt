project(mvptoken)

set(EOSIO_WASM_OLD_BEHAVIOR "Off")
find_package(eosio.cdt)

add_contract( mvptoken mvptoken mvptoken.cpp )
target_include_directories( mvptoken PUBLIC ${CMAKE_SOURCE_DIR}/../include )
target_ricardian_directory( mvptoken ${CMAKE_SOURCE_DIR}/../ricardian )