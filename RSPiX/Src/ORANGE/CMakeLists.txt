add_library(orange STATIC
	GameLib/ANIMSPRT.cpp
	Attribute/attribute.cpp
	GUI/btn.cpp
	Channel/channel.cpp
	color/colormatch.cpp
	DirtRect/DirtRect.cpp
	color/dithermatch.cpp
	GUI/dlg.cpp
	GUI/edit.cpp
	File/file.cpp
	QuickMath/FixedPoint.cpp
	GUI/guiItem.cpp
	IFF/iff.cpp
	ImageTools/lasso.cpp
	Laymage/laymage.cpp
	GUI/ListBox.cpp
	GUI/ListContents.cpp
	Meter/meter.cpp
	MsgBox/MsgBox.cpp
	GUI/MultiBtn.cpp
	MultiGrid/MultiGrid.cpp
	MultiGrid/MultiGridIndirect.cpp
	GUI/ProcessGui.cpp
	Debug/profile.cpp
	GUI/PushBtn.cpp
	QuickMath/QuickMath.cpp
	GameLib/Region.cpp
	RString/rstring.cpp
	GUI/scrollbar.cpp
	GameLib/SHAPES.cpp
	Parse/SimpleBatch.cpp
	GameLib/SPRITE.cpp
	str/str.cpp
	GUI/txt.cpp)

target_link_libraries(orange blue)
