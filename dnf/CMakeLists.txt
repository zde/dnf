FILE(GLOB dnf_SRCS *.py)
INSTALL (FILES ${dnf_SRCS} DESTINATION ${PYTHON_INSTALL_DIR}/dnf)
# const.py is generated so the glob alone won't see it:
INSTALL (FILES const.py DESTINATION ${PYTHON_INSTALL_DIR}/dnf)

ADD_SUBDIRECTORY (rpmUtils)
ADD_SUBDIRECTORY (yum)
ADD_SUBDIRECTORY (cli)
