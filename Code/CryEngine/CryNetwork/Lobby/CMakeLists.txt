set(THIS_PROJECT CryLobby)

project( ${THIS_PROJECT} )

#START-FILE-LIST
# File List auto generated by waf2cmake.py, do not modify manually.

set (SourceGroup_DurangoLive
	DurangoLive/CryDurangoLiveLobby.cpp
	DurangoLive/CryDurangoLiveLobby.h
	DurangoLive/CryDurangoLiveLobbyPacket.h
	DurangoLive/CryDurangoLiveLobbyUI.cpp
	DurangoLive/CryDurangoLiveLobbyUI.h
	DurangoLive/CryDurangoLiveMatchMaking.cpp
	DurangoLive/CryDurangoLiveMatchMaking.h
	DurangoLive/CryDurangoLiveOnlineStorage.cpp
	DurangoLive/CryDurangoLiveOnlineStorage.h
	DurangoLive/DurangoChat/ChatIntegrationLayer.cpp
	DurangoLive/DurangoChat/ChatIntegrationLayer.h
	DurangoLive/platform.cpp
	DurangoLive/platform.h
)
source_group("DurangoLive" FILES ${SourceGroup_DurangoLive})


set (SourceGroup_LAN
	LAN/CryLANLobby.cpp
	LAN/CryLANLobby.h
	LAN/CryLANMatchMaking.cpp
	LAN/CryLANMatchMaking.h
)
source_group("LAN" FILES ${SourceGroup_LAN})


set (SourceGroup_OrbisPSN
	PSNOrbis/CryPSN2Friends.cpp
	PSNOrbis/CryPSN2Friends.h
	PSNOrbis/CryPSN2Lobby.cpp
	PSNOrbis/CryPSN2Lobby.h
	PSNOrbis/CryPSN2LobbyUI.cpp
	PSNOrbis/CryPSN2LobbyUI.h
	PSNOrbis/CryPSN2MatchMaking.cpp
	PSNOrbis/CryPSN2MatchMaking.h
	PSNOrbis/CryPSN2Response.cpp
	PSNOrbis/CryPSN2Response.h
	PSNOrbis/CryPSN2Reward.cpp
	PSNOrbis/CryPSN2Reward.h
	PSNOrbis/CryPSN2Stats.cpp
	PSNOrbis/CryPSN2Stats.h
	PSNOrbis/CryPSN2Support.cpp
	PSNOrbis/CryPSN2Support.h
	PSNOrbis/CryPSN2WebApi.cpp
	PSNOrbis/CryPSN2WebApi.h
	PSNOrbis/CryPSN2WebApi_ActivityFeed.cpp
	PSNOrbis/CryPSN2WebApi_ActivityFeed.h
	PSNOrbis/CryPSN2WebApi_FriendsList.cpp
	PSNOrbis/CryPSN2WebApi_FriendsList.h
	PSNOrbis/CryPSN2WebApi_Presence.cpp
	PSNOrbis/CryPSN2WebApi_Presence.h
	PSNOrbis/CryPSN2WebApi_RecentPlayers.cpp
	PSNOrbis/CryPSN2WebApi_RecentPlayers.h
	PSNOrbis/CryPSN2WebApi_Session.cpp
	PSNOrbis/CryPSN2WebApi_Session.h
	PSNOrbis/CryPSN2WebApi_Store.cpp
	PSNOrbis/CryPSN2WebApi_Store.h
)
source_group("OrbisPSN" FILES ${SourceGroup_OrbisPSN})


set (SourceGroup_Root
	CryDedicatedServer.cpp
	CryDedicatedServer.h
	CryDedicatedServerArbitrator.cpp
	CryDedicatedServerArbitrator.h
	CryFriends.cpp
	CryFriends.h
	CryFriendsManagement.cpp
	CryFriendsManagement.h
	CryHostMigration.cpp
	CryHostMigration.h
	CryLobby.cpp
	CryLobby.h
	CryLobbyDLL.cpp
	CryLobbyUI.cpp
	CryLobbyUI.h
	CryMatchMaking.cpp
	CryMatchMaking.h
	CryRebroadcaster.cpp
	CryRebroadcaster.h
	CryReward.cpp
	CryReward.h
	CrySharedLobbyPacket.h
	CrySignIn.cpp
	CrySignIn.h
	CryStats.cpp
	CryStats.h
	CryTCPService.cpp
	CryTCPService.h
	CryTCPServiceFactory.cpp
	CryTCPServiceFactory.h
	CryVoice.cpp
	CryVoice.h
	ICryLobbyPrivate.h
	ICryMatchMakingPrivate.h
	LobbyCVars.cpp
	LobbyCVars.h
	StdAfx.cpp
	StdAfx.h
	resource.h
)


set (SourceGroup_Steam
	Steam/CrySteamFriends.cpp
	Steam/CrySteamFriends.h
	Steam/CrySteamFriendsManagement.cpp
	Steam/CrySteamFriendsManagement.h
	Steam/CrySteamLobby.cpp
	Steam/CrySteamLobby.h
	Steam/CrySteamMatchMaking.cpp
	Steam/CrySteamMatchMaking.h
	Steam/CrySteamReward.cpp
	Steam/CrySteamReward.h
	Steam/CrySteamStats.cpp
	Steam/CrySteamStats.h
	Steam/CrySteamVoice.h
)
source_group("Steam" FILES ${SourceGroup_Steam})


# Support unity build with uber files
set(CryLobby_durango_live_uber_cpp ${SourceGroup_DurangoLive}  )
enable_unity_build( "CryLobby_durango_live_uber.cpp" CryLobby_durango_live_uber_cpp )

set(CryLobby_orbis_psn_uber_cpp ${SourceGroup_OrbisPSN}  )
enable_unity_build( "CryLobby_orbis_psn_uber.cpp" CryLobby_orbis_psn_uber_cpp )

set(CryLobby_steam_uber_cpp ${SourceGroup_Steam}  )
enable_unity_build( "CryLobby_steam_uber.cpp" CryLobby_steam_uber_cpp )

set(CryLobby_uber_0_cpp ${SourceGroup_LAN} ${SourceGroup_Root}  )
enable_unity_build( "CryLobby_uber_0.cpp" CryLobby_uber_0_cpp )

set(NoUberFile  )


set (SOURCES
	${CryLobby_durango_live_uber_cpp}
	${CryLobby_orbis_psn_uber_cpp}
	${CryLobby_steam_uber_cpp}
	${CryLobby_uber_0_cpp}
	${NoUberFile}
)
#END-FILE-LIST


include_directories( ${CMAKE_CURRENT_SOURCE_DIR} )
include_directories( ${CMAKE_CURRENT_SOURCE_DIR}/.. )

include_directories( ${SDK_DIR}/Steamworks/public )

# Exclude files from Build
if (NOT ORBIS)
	set_source_files_properties( ${SourceGroup_OrbisPSN} PROPERTIES HEADER_FILE_ONLY TRUE)
endif()

if (NOT DURANGO)
	set_source_files_properties( ${SourceGroup_DurangoLive} PROPERTIES HEADER_FILE_ONLY TRUE)
endif()

if (DURANGO)
	# Enable Unicode on Durango
	add_definitions(-D_UNICODE)
endif()

add_library( ${THIS_PROJECT} ${SOURCES})

if (DURANGO)
	target_link_libraries( ${THIS_PROJECT} Ws2_32 uuid )
elseif (WIN64)
	target_link_libraries( ${THIS_PROJECT} Ws2_32 )
	if (OPTION_USE_STEAM)
		target_link_libraries( ${THIS_PROJECT} ${SDK_DIR}/Steamworks/redistributable_bin/win64/steam_api64.lib )
	endif()
elseif (WIN32)
	target_link_libraries( ${THIS_PROJECT} Ws2_32 )
	if (OPTION_USE_STEAM)
		target_link_libraries( ${THIS_PROJECT} ${SDK_DIR}/Steamworks/redistributable_bin/steam_api.lib )
	endif()
endif()

USE_MSVC_PRECOMPILED_HEADER( ${THIS_PROJECT} "StdAfx.h" "StdAfx.cpp" )

SET_PLATFORM_TARGET_PROPERTIES( ${THIS_PROJECT} )

if (DURANGO)
	# add winmd search paths
	set_property( TARGET ${THIS_PROJECT} APPEND_STRING PROPERTY VS_CONFIG_PROPERTY_GROUP_ReferencePath ";${DURANGO_SDK}/Extensions/Xbox Services API/8.0/References/CommonConfiguration/neutral")
	set_property( TARGET ${THIS_PROJECT} APPEND_STRING PROPERTY VS_CONFIG_PROPERTY_GROUP_ReferencePath ";${CMAKE_CURRENT_SOURCE_DIR}/DurangoLive/DurangoChat/Microsoft.Xbox.GameChat")
endif()