
# scripts for RPM package
#
if ("${CPACK_GENERATOR}" STREQUAL "RPM")
	# chmod +x 655
	install (FILES tarantool_box DESTINATION etc/init.d
                 PERMISSIONS
		 OWNER_READ OWNER_WRITE
		 GROUP_READ GROUP_EXECUTE
		 WORLD_READ WORLD_EXECUTE)
	# chmod +x 755
	install (FILES tarantool_box.sh DESTINATION bin
                 PERMISSIONS
		 OWNER_READ OWNER_WRITE OWNER_EXECUTE
		 GROUP_READ GROUP_EXECUTE
		 WORLD_READ WORLD_EXECUTE)
endif()
