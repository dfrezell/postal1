add_library(green STATIC
	Hot/hot.cpp
	Image/Image.cpp
	Image/Imagecon.cpp
	Image/ImageFile.cpp
	InputEvent/InputEvent.cpp
	Mix/mix.cpp
	Mix/MixBuf.cpp
	Image/pal.cpp
	Image/PalFile.cpp
	Sample/sample.cpp
	Snd/snd.cpp
	SndFx/SndFx.cpp
	Task/task.cpp
	3D/pipeline.cpp
	3D/render.cpp
	3D/types3d.cpp
	3D/zbuffer.cpp
	BLiT/alphablit.cpp
	BLiT/BLIT.cpp
	BLiT/BLITINIT.cpp
	BLiT/BLiTT.cpp
	BLiT/CFNT.cpp
	BLiT/Fspr1.cpp
	BLiT/FSPR8.cpp
	BLiT/line.cpp
	BLiT/mono.cpp
	BLiT/Rotate96.cpp
	BLiT/RPrint.cpp
	BLiT/ScaleFlat.cpp)

target_link_libraries(green blue)
