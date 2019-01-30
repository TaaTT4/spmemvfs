add_library(${PROJECT_NAME}
		spmemvfs.h
		spmemvfs.c
)

set_property(TARGET ${PROJECT_NAME} PROPERTY DEBUG_POSTFIX _d)
set_property(TARGET ${PROJECT_NAME} PROPERTY COMPILE_PDB_NAME_DEBUG ${PROJECT_NAME}_d)


install(TARGETS ${PROJECT_NAME} ARCHIVE DESTINATION lib/$<CONFIG>)

install(FILES spmemvfs.h DESTINATION include)
