TARGET  = main
SRC 	= $(wildcard *.cpp)
OBJ 	= $(SRC:.cpp=.o)

LD 		= g++

GENERICCXXFLAGS = 
PROJCXXFLAGS = -pthread -I/usr/include/gstreamer-0.10 -I/usr/include/glib-2.0 -I/usr/lib/x86_64-linux-gnu/glib-2.0/include -I/usr/include/libxml2

GENERICLDFLAGS = 
PROJLDFLAGS = -pthread -lgstreamer-0.10 -lgobject-2.0 -lgmodule-2.0 -lgthread-2.0 -lxml2 -lglib-2.0

CXXFLAGS = $(GENERICCXXFLAGS) $(PROJCXXFLAGS)
LDFLAGS = $(GENERICLDFLAGS) $(PROJLDFLAGS)

$(TARGET): $(OBJ)
	$(LD) $(OBJ) -o $(TARGET) $(LDFLAGS)

clean: 
	rm -f $(TARGET) $(OBJ)

.PHONY:
	clean $(TARGET)
