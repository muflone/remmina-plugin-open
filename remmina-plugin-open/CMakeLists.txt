#     Project: Remmina Plugin OPEN
# Description: Remmina protocol plugin to open a document with its associated
#              application.
#      Author: Fabio Castelli (Muflone) <muflone@vbsimple.net>
#   Copyright: 2011-2016 Fabio Castelli (Muflone)
#     License: GPL-2+
#
# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful, but WITHOUT
# ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or
# FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for
# more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.

set(REMMINA_PLUGIN_SRCS
  src/remmina_plugin.c
)
add_library(remmina-plugin-open ${REMMINA_PLUGIN_SRCS})
set_target_properties(remmina-plugin-open PROPERTIES PREFIX "")
include_directories(${CMAKE_SOURCE_DIR}/remmina-plugins)
target_link_libraries(remmina-plugin-open ${REMMINA_COMMON_LIBRARIES})

install(TARGETS remmina-plugin-open DESTINATION ${REMMINA_PLUGINDIR})

set(APPICON16_EMBLEMS_DIR "${REMMINA_DATADIR}/icons/hicolor/16x16/emblems")
install(FILES 16x16/emblems/remmina-open.png DESTINATION ${APPICON16_EMBLEMS_DIR})

set(APPICON22_EMBLEMS_DIR "${REMMINA_DATADIR}/icons/hicolor/22x22/emblems")
install(FILES 22x22/emblems/remmina-open.png DESTINATION ${APPICON22_EMBLEMS_DIR})
