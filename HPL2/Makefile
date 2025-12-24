CXX=g++
INCLUDE = -I./include -I./dependencies/include -I./dependencies/include/AL  -I./dependencies/include/HaptX
PLATFORM ?= linux
LIBS = -lSDL2 -lglew -lfltk -lfltk_images -lIL -ljpeg -lNewton -logg -lopenal -ltheora -lvorbis -lvorbisfile -L./dependencies/lib/$(PLATFORM)/lib64/
CXX_FLAGS = -Wall -Wconversion -Wsign-conversion
CXX_DEBUG =
TARGET = libhlp.a

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(OBJ)

$(OBJ): %.o: %.cpp
	$(CXX) -o $@ $(CXX_FLAGS) $(CXX_DEBUG) $(INCLUDE) -c $^ $(LIBS)