cmake_minimum_required(VERSION 2.8.12)

project(POSTAL)

add_definitions(-DTARGET=POSTAL_2015 -DLOCALE=US -DALLOW_TWINSTICK)

if (UNIX)
	add_definitions(-DPLATFORM_UNIX)
	add_compile_options(-arch i386)
endif(UNIX)

if (APPLE)
	add_definitions(-DPLATFORM_MACOSX)
	add_compile_options(-mmacosx-version-min=10.5)
endif (APPLE)

add_subdirectory(RSPiX)
add_subdirectory(WishPiX)

add_executable(postal1-bin
    AnimThing.cpp 
	ball.cpp 
	barrel.cpp 
	bouy.cpp 
	character.cpp 
	chunk.cpp 
	deathWad.cpp 
	demon.cpp 
	dispenser.cpp 
	doofus.cpp 
	dude.cpp 
	explode.cpp 
	fire.cpp 
	fireball.cpp 
	firebomb.cpp 
	flag.cpp 
	flagbase.cpp 
	grenade.cpp 
	heatseeker.cpp 
	hood.cpp 
	item3d.cpp 
	mine.cpp 
	napalm.cpp 
	navnet.cpp 
	ostrich.cpp 
	person.cpp 
	PowerUp.cpp 
	pylon.cpp 
	rocket.cpp 
	sentry.cpp 
	SndRelay.cpp 
	SoundThing.cpp 
	thing.cpp 
	Thing3d.cpp 
	trigger.cpp 
	warp.cpp 
	weapon.cpp 
	alphablitforpostal.cpp 
	Anim3D.cpp 
	BufQ.cpp 
	bulletFest.cpp 
	camera.cpp 
	crawler.cpp 
	cutscene.cpp 
	encrypt.cpp 
	gameedit.cpp 
	GameSettings.cpp 
	grip.cpp 
	IdBank.cpp 
	InputSettings.cpp 
	InputSettingsDlg.cpp 
	keys.cpp 
	Log.cpp 
	logtab.cpp 
	MemFileFest.cpp 
	MenuSettings.cpp 
	MenuTrans.cpp 
	net.cpp 
	NetBrowse.cpp 
	NetClient.cpp 
	NetDlg.cpp 
	netmsgr.cpp 
	NetServer.cpp 
	organ.cpp 
	Personatorium.cpp 
	ProtoBSDIP.cpp 
	realm.cpp 
	scene.cpp 
	score.cpp 
	settings.cpp 
	smash.cpp 
	socket.cpp 
	StockPile.cpp 
	TexEdit.cpp 
	toolbar.cpp 
	TriggerRegions.cpp 
	update.cpp 
	yatime.cpp 
	aivars.cpp 
	band.cpp 
	credits.cpp 
	game.cpp 
	input.cpp 
	localize.cpp 
	main.cpp 
	menus.cpp 
	play.cpp 
	SampleMaster.cpp 
	title.cpp)

target_link_libraries(postal1-bin PRIVATE blue cyan green orange wishpix)
target_include_directories(postal1-bin PRIVATE ${PROJECT_SOURCE_DIR} RSPiX/Inc)

if (APPLE)
    set_target_properties(postal1-bin PROPERTIES
		LINK_FLAGS ${LINK_FLAGS} "-arch i386 -mmacosx-version-min=10.5")
    target_link_libraries(postal1-bin PRIVATE
		${CMAKE_CURRENT_SOURCE_DIR}/SDL2/libs/macosx/libSDL2-2.0.0.dylib)
endif (APPLE)
