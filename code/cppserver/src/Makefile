# 检测结果处理器Makefile
# ziqing.zp@alibaba-inc.com
# 2018.06.26


TARGET = Server
SOURCES = $(wildcard *.cc)
OBJECTS = $(SOURCES:.cc=.o)

INCLUDE = -I/usr/local/include -I.
CXXFLAGS = $(INCLUDE) -O0 -g
LDFLAGS = -L/usr/local/lib -lpthread


all: $(TARGET)

$(TARGET):$(OBJECTS)
	$(CXX) -o $(TARGET) $(OBJECTS) $(CXXFLAGS) $(LDFLAGS) 

$(OBJECTS):%.o :%.cc
	$(CXX) -o $@ -c $< $(CXXFLAGS)


install:
	

clean:
	rm $(OBJECTS) $(TARGET) -f


