if(QBDI_PLATFORM_LINUX OR QBDI_PLATFORM_ANDROID)
  target_sources(QBDIPreload PRIVATE "${CMAKE_CURRENT_LIST_DIR}/linux_X86_64.c")
elseif(QBDI_PLATFORM_OSX)
  target_sources(QBDIPreload PRIVATE "${CMAKE_CURRENT_LIST_DIR}/osx_X86_64.c")
else()
  message(FATAL_ERROR "No QBDIPreload for architecture ${QBDI_ARCH}")
endif()
